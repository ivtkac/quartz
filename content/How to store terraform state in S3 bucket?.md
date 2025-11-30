---
title: How to store terraform state in S3 bucket?
created: 2025-11-30
tags:
  - 🦮how-to
  - terraform
  - aws
  - config
aliases:
---
prev:: [[Що потрібно для зберігання terraform state віддалено у AWS?]]

Для зберігання стану [[Terraform]] віддалено [[AWS S3]] потрібно налаштувати серверну частину S3 всередині блоку `terraform`. Цей блок **не може** використовувати змінні (`var.*`) або функції.

Перед збереженням відалено, потрібно створити подібну конфігурацію з S3 bucket та Dynamo Table:

```terraform
terraform {
	required_providers {
		aws = {
			source = "hashicorp/aws"
			version = "~> 5.0"
		}	
	}
}

provider "aws" {
	profile = "default"
	region = "eu-central-1"
}

resource "aws_s3_bucket" "terraform_state" {
	bucket = "your-unique-terraform-state-bucket-name"
	tags = {
		Name = "Terraform State Bucket"	
		Environment = "Production"
	}
	
	lifecycle {
		prevent_destroy = true	
	}
}

resource "aws_s3_bucket_versioning" "terraform_state" {
	bucket = aws_s3_bucket.terraform_state.id
	versioning_configuration {
		status = "Enabled"	
	}
}

resource "aws_s3_bucket_server_side_encyrption_configuration" "terraform_state" {
	bucket = aws_s3_bucket.terraform_state.id
	
	rule {
		apply_server_side_encryption_by_default {
			sse_algorithm = "AES256"	
		}	
	}
}

resource "aws_s3_bucket_public_access_block" "terraform_state" {
  bucket = aws_s3_bucket.terraform_state.id	
  
  block_public_acls       = true
  block_public_policy     = true
  ignore_public_acls      = true
  restrict_public_buckets = true
}

resource "aws_dynamodb_table" "terraform_lock" {
  name         = "terraform-state-lock"
  billing_mode = "PAY_PER_REQUEST"
  hash_key     = "LockID"

  attribute {
    name = "LockID"
    type = "S"
  }

  tags = {
    Name        = "Terraform State Lock Table"
    Environment = "Production"
  }
}
```

Після  `terraform init`, `terraform plan`, `terraform apply`, можна прибрати ці ресурси і залишити:

```
terraform {
  backend "s3" {
    bucket         = "your-unique-terraform-state-bucket-name"
    key            = "terraform.tfstate"
    region         = "eu-central-1"
    encrypt        = true
    dynamodb_table = "terraform-state-lock"
  }
}
```