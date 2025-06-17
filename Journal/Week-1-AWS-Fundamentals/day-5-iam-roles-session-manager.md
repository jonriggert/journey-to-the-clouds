# Day 5: IAM Roles, EC2 Identity Federation, and Session Manager

## ✅ Tasks Completed
- Created IAM role: `EC2S3SSMAccessRole`
  - Attached `AmazonS3FullAccess`
  - Attached `AmazonSSMManagedInstanceCore`
- Launched EC2 instance: `role-demo-ec2` using Amazon Linux 2
- Confirmed instance was in a subnet with internet access
- Attached IAM role to instance and verified via EC2 metadata
- Used **Session Manager** to connect (no SSH or `.pem` file required)
- Created files in home directory (`/home/ssm-user`) from session
- Uploaded files to S3 bucket (`cloud-intern-jon-reports`) using instance role

## 🧪 Commands Used
```bash
# Create test file
echo "This file was uploaded from Session Manager using an IAM role!" > ~/test-from-ssm.txt

# Upload to S3
aws s3 cp ~/test-from-ssm.txt s3://cloud-intern-jon-reports/

# Confirm upload
aws s3 ls s3://cloud-intern-jon-reports/