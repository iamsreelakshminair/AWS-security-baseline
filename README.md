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
 


