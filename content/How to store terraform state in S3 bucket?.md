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
Storing your [[Terraform]] state remotely in an [[AWS S3]] bucket is the **recommended best practice** for team environments. It provides durability, scalability, and enables **state locking** to prevent concurrent state modifications.

You must **manually** (or via a separate, minimal Terraform configuration) create two key resources before running your main configuration:

1. 🗃️ **S3 Bucket** (for State Storage) 
	- *versioning* must be enabled (for state recovery)
	- *server-side-encryption* ([[SSE]])  should be enabled (e.g. AES-256)
	- *public access* should be **blocked**
2. 🔒 **[[Dynamodb]] Table** (for State Locking)
	- prevents multiple users from running `terraform apply` simultaneously
	- must have a **primary key** named `LockID` (of type String)


You must configure the S3 backend inside the `terraform` block. This block **cannot** use variables (`var.*`) or functions.

```terraform
terraform {
	required 
}
```