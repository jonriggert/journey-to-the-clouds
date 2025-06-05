# Basic Navagation Commands

## Setup to setup credentials and store keys securely (avoid using root)

aws configure
aws configure list

## List all S3 buckets

aws s3 ls
aws s3api list-buckets --output table

## List all IAM users or groups

aws iam list-users
aws iam list-groups
aws iam get-user --user-name <name>

## List EC2 instances

aws ec2 describe-instances --query "Reservations[*].Instances[*].[InstanceID,State.Name,Tags]" --output table

## List available regions

aws ec2 describe-regions --output table
aws ec2 describe-availability-zones

## Use help built-in

aws ec2 help
aws ec2 describe-instances help

### CLI Output Format Options
- JSON (default): scripting, logging, APIs
- table: human readable but not machine-friendly
- text: very simple, pipe-friendly, poor formatting and confusing with nested objects