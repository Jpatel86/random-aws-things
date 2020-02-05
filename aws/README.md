# AWS Terraform set up

## Download terraform 

```bash
brew install terraform
```

## Set up AWS account

First, create an aws account and set up an IAM user. 

Second, configure aws profile.

```bash
cat ~/.aws/config

[personal]
region = us-west-2
output = json

cat ~/.aws/credentials

[personal]
aws_access_key_id     = XYZ...
aws_secret_access_key = abcd..
```

## Create S3 bucket for terraform backend storage

```bash
AWS_BUCKET_NAME=aws-terraform-backend

aws s3api create-bucket --bucket $AWS_BUCKET_NAME --profile personal
```