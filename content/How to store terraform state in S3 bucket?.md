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
 ![[Що потрібно для зберігання terraform state віддалено у AWS?]]

Для зберігання стану [[Terraform]] віддалено [[AWS S3]] потрібно налаштувати серверну частину S3 всередині блоку `terraform`. Цей блок **не може** використовувати змінні (`var.*`) або функції.



Але для початку потрібно

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

resource "aws_s3_bucket_server_side_encyrption_configuration"
```