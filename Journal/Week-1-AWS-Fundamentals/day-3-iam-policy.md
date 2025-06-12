# Day 3: IAM Policy - Least Privilege Lab

## ✅ Tasks Completed
- Created IAM user `intern-contractor`
- Wrote custom IAM policy for S3 `PutObject` only
- Verified that uploads work but listing files fails as expected

## 🔒 Policy Snippet
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowPutOnly",
            "Effect": "Allow",
            "Action": "s3:PutObject",
            "Resource": "arn:aws:s3:::cloud-intern-jon-reports/*"
        }
    ]
}