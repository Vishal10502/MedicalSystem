# GitHub actions:
## Task 2(V2): 
In this task with the help of github actions we are creating a s3 bucket and copying .war file into that bucket. <br>

## Create main.tf write the below content: <br>

```

terraform {
  required_version = ">= 0.12.26"
}

provider "aws" {
  access_key = "AKIA4DN5TV67YT3EE52A"
  secret_key = "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"
  region     = "us-east-1"
}

resource "aws_s3_bucket" "b" {
  bucket = "mohit-bkt-22-august"
  acl    = "private"

  versioning {
    enabled = true
  }
}

```









