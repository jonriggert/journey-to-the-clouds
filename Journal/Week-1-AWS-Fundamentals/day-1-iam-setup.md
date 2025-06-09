# Day 1: IAM Setup & CLI Configuration

## ✅ Tasks Completed
- Created IAM user with admin privileges
- Enabled MFA for root and IAM user
- Installed and configured AWS CLI via VS Code terminal

## 🖥️ CLI Output
```bash
aws sts get-caller-identity
# (paste output here)
{
    "UserId": "AIDATFBMPGN724IVQDZ4H",
    "Account": "216989119359",
    "Arn": "arn:aws:iam::216989119359:user/amazing.admin.jon"
}

aws s3 ls
# (paste output here, even if it’s empty)
2025-05-29 09:59:41 jon-aws-lab-cli-bucket
2025-05-29 09:42:23 jon-aws-lab-day2
2025-05-30 08:33:31 jon-s3-day-3-cli
2025-05-30 09:05:09 jon-s3-day-3-cli-v2
2025-05-30 09:08:50 jon-s3-day-3-cli-v3

# What I learned:
- sts means Security Token Service, and confirms which credentials I am using. 
- MFA and least privilege access are standard best practices.
- You should ALWAYS verify your identity before running CLI commands. 