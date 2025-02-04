Terraform Module to provision an AWS EC2 instance with the latest amazon linux 2023 ami and installed docker in it.

Not intended for production use. It is an example module.

It is just for showing how to create a publish module in Terraform Registry.
 
Usage:

```hcl

provider "aws" {
  region = "us-east-1"
}

module "docker_instance" {
    source = "AizazZaidee/docker-instance/aws"
    version = "x.y.z"  # Replace with the latest version or specific version
    key_name = "<Your SSH Keypair name>"
}
```

To check your available key pairs, run:
```go
aws ec2 describe-key-pairs --query "KeyPairs[*].KeyName" --output text
```
