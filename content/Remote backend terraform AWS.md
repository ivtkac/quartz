---
created: 2025-12-01
title: How to store terraform state in AWS?
tags:
  - 🦮how-to
  - terraform
  - aws
  - config
aliases:
---
prev:: [[Що потрібно для зберігання terraform state віддалено у AWS?]]

> [!warning] Before run backend we need boostrap bucket and dynamo db

```tf
terraform {
	backend "s3" {
		bucket = "my-tf-state"	
		key = "tf-infra/terraform.tfstate"
		region = "us-east-1"
		dynamodb_table = "terraform-state-locking"
		encrypt = true
	}
}
```

## 1. Bootstraping

1. default to local (without remote backend)
2. defined [[AWS S3]] and [[Dynamodb]]

```tf
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
```

```tf
resource "aws_dynamodb_table" "terraform_locks" {
	name = "terraform-state-locking"
	billing_mode = "PAY_PER_REQUEST"
	hash_key = "LockID"
	attribute {
		name = "LockID"	
		type = "S"
	}
}
```

2. Specified as S3 bucket
```tf
terraform {
	backend "s3" {
		bucket = "my-tf-state",
		key = "tf-infra/terraform.tfstate"
		region = "us-east-1"
		dynamodb_table = "terraform-state-locking"
		encrypt = true
	}
}
```

- `terraform init`
- `terraform plan`