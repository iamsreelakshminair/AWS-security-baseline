# AWS-security-baseline
This guide provides controls for start-up companies to manage security risks in their AWS Cloud account without much effort. It is designed for single-account architectures that can be easily modified or migrated to multi-account architectures as the organization grows.

The AWS Startup Security Baseline (SSB) is a series of measures that provide a secure foundation for businesses to build on AWS without compromising their flexibility. These measures are designed to enhance security by protecting credentials, enabling logging and visibility, managing contact information, and setting basic data boundaries.

The AWS SSB has two types of controls: account and workload. Account controls keep the AWS account safe by guiding users on how to set up user access, policies, and permissions, and how to monitor the account for suspicious activity. Workload controls protect resources and code in the cloud, including applications, backend processes, and data, by providing recommendations such as encryption and access reduction.

# Securing your account

This section provides guidelines and precautions to ensure the safety of your AWS account. It suggests using IAM users, groups, and roles for access, avoiding the root user, and implementing multi-factor authentication. Additionally, it recommends confirming contact information with AWS and setting up monitoring services like AWS Trusted Advisor and Amazon GuardDuty to detect any unauthorized activity.

## This section contains the following topics:

 * [ACCT.01 – Set account-level contacts to valid email distribution lists](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-01.html)
 * [ACCT.02 – Restrict use of the root user](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-02.html)
 * [ACCT.03 – Configure console access for each user](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-03.html)
 * [ACCT.04 – Assign permissions](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-04.html)
 * [ACCT.05 – Require multi-factor authentication (MFA) to log in](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-05.html)
 * [ACCT.06 – Enforce a password policy](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-06.html)
 * [ACCT.07 – Deliver CloudTrail logs to a protected S3 bucket](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-07.htm)
 * [ACCT.08 – Prevent public access to private S3 buckets](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-08.html)
 * [ACCT.09 – Delete unused VPCs, subnets, and security groups](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-09.html)
 * [ACCT.10 – Configure AWS Budgets to monitor your spending](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-10.html)
 * [ACCT.11 – Enable and respond to GuardDuty notifications](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-11.html)
 * [ACCT.12 – Monitor for and resolve high-risk issues by using Trusted Advisor](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-12.html)

# Section Overview
1. Accurate Account Information : Accurate account information prevents you from losing access to your account. When AWS needs to contact you about your AWS account , we use the contact information defined in the AWS Management Console, including the email address used to create the account and those listed under Alternate Contacts.
2. Protect the Root User :	Your root user (the email you used to register the AWS account) is very powerful and grants unlimited access to your account and resources. In this module, we will work to protect your root user.
3. Create Users for Human Identities :	Instead of using your root user, you should create and use either an IAM Admin User or an SSO Admin User for day-to-day tasks.
4. Use IAM User Groups for Human Operator Permissions: User Groups enable applying permission policies to the collection of IAM Users that are within the group. Create User Groups that align to human operator job functions and attach appropriate AWS-managed policies or AWS-defined Permission Sets to get started with granting least privilege.
5. Turn CloudTrail on	: Logging and monitoring are important parts of a robust security plan. AWS CloudTrail  monitors and records account activity across your AWS infrastructure, ensuring that you know who is doing what and where in your AWS account.
6. Prevent Public Access to Private S3 Buckets :	Prevent public access to your private S3 buckets due to bucket policy misconfiguration by enabling the Block Public Access setting for each bucket.
7. Configure Alarms	: In this workshop, we will set up a billing alarm and an alarm for root account use. Thhese alarms can notify you if a malicious actor has accessed your account and deployed resources.
8. Delete unused VPCs, Subnets & Securtiy Groups :	Delete or disable any resources that are not being used to reduce the opportunity for security issues.
9. Enable AWS Trusted Advisor :	AWS Trusted Advisor  passively scans your AWS infrastructure for high risk or high impact issues related to security, performance, cost, and reliability, with detailed information about affected resources and remediation recommendations.
10. Enable GuardDuty :	Enable GuardDuty and respond to findings to stop malicious or unauthorized behavior occurring within your AWS account.

# Securing your workloads
This section provides guidance on how to secure your workloads on AWS while you are developing them. It focuses on best practices for managing application secrets, limiting access to private resources, and using encryption to protect data both in transit and at rest.
 * [WKLD.01 – Use IAM roles for compute environment permissions](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-01.htm)
 * [WKLD.02 – Restrict credential usage scope with resource-based policies permissions](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-02.html)
 * [WKLD.03 – Use ephemeral secrets or a secrets-management service](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-03.html)
 * [WKLD.04 – Prevent application secrets from being exposed](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-04.htm)
 * [WKLD.05 – Detect and remediate exposed secrets](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-05.html)
 * [WKLD.06 – Use Systems Manager instead of SSH or RDP](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-06.html)
 * [WKLD.07 – Log data events for S3 buckets with sensitive data](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-07.html)
 * [WKLD.08 – Encrypt Amazon EBS volumes](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-08.html)
 * [WKLD.09 – Encrypt Amazon RDS databases](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-09.html)
 * [WKLD.10 – Deploy private resources into private subnets](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-10.html)
 * [WKLD.11 – Restrict network access by using security groups](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-11.html)
 * [WKLD.12 – Use VPC endpoints to access supported services](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-12.html)
 * [WKLD.13 – Require HTTPS for all public web endpoints](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-13.html)
 * [WKLD.14 – Use edge-protection services for public endpoints](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-14.html)
 * [WKLD.15 – Define security controls in templates and deploy them by using CI/CD practices](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/wkld-15.html)

 

