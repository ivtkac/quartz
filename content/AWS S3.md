---
created: 2025-11-21
title: AWS S3
tags:
  - aws
aliases:
---
- об'єктне сховище для збереження інформації у вигляді об'єктів

## Terraform

```tf
terraform {
	backend "s3" {
		bucket = "org-tf-state"	
		key = "tf-infra/terraform.tfstate"
		region = "us-east-1"
		dynamodb_table = "terraform-state-locking"
		encrypt = true
	}
}
```