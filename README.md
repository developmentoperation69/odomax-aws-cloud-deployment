# AWS Cloud Deployment Project

## Project Overview
This project was completed as the final project of the Codomax Digital Solution DevOps & AWS Internship.

The objective was to deploy a web application on AWS, configure secure access to AWS resources, and implement basic cloud monitoring.

## AWS Services Used

1. **Amazon EC2** – Hosts the web application using Amazon Linux 2023 and Nginx.
2. **Amazon S3** – Stores project files and provides object storage.
3. **AWS IAM** – Manages permissions through an EC2 IAM role.
4. **Amazon CloudWatch** – Monitors EC2 metrics and generates CPU utilization alarms.
5. **Amazon SNS** – Used as the notification service for CloudWatch alarms.

## Infrastructure Details

- AWS Region: Asia Pacific (Sydney) – `ap-southeast-2`
- EC2 Instance: `codomax-web-server`
- Operating System: Amazon Linux 2023
- Web Server: Nginx
- S3 Bucket: `usama-s3-portfolio-2026`
- IAM Role: `EC2-WebServer-Role`
- CloudWatch Alarm: `codomax-ec2-cpu-high`
- CloudWatch Dashboard: `codomax-aws-monitoring`
- SNS Topic: `codomax-cpu-alerts`

## Security Configuration

- Created an IAM role and attached it to the EC2 instance.
- Configured limited S3 permissions for the EC2 role.
- Used IAM role-based access instead of storing AWS access keys on the server.
- Kept S3 Block Public Access enabled.
- Used server-side encryption (SSE-S3) for S3 objects.
- Configured EC2 security group access for web traffic.

## Monitoring and Alerts

Configured Amazon CloudWatch to monitor:

- EC2 CPU Utilization
- Network In
- Network Out

Created a CPU utilization alarm that triggers when average CPU usage exceeds 80% over a 5-minute period.

An SNS topic was configured for alarm notifications.

## Testing and Verification

- Verified that the Nginx web server was running.
- Verified HTTP response from the EC2-hosted website.
- Verified EC2 access to the S3 bucket using its IAM role.
- Uploaded and downloaded a test object from S3.
- Verified S3 object encryption.
- Created a CloudWatch dashboard and CPU utilization alarm.

## Architecture Diagram

See the AWS architecture diagram here:

[Download AWS Architecture Diagram](Codomax-AWS-Cloud-Deployment-Architecture.pdf)

## Project Learning Outcomes

- AWS EC2 deployment and web server configuration
- S3 bucket management and object storage
- IAM roles and least-privilege permissions
- EC2 and S3 integration
- CloudWatch monitoring and alarms
- SNS notification configuration
- Basic AWS cloud security

## Author

Codomax Digital Solution – DevOps & AWS Internship

GitHub Repository: https
