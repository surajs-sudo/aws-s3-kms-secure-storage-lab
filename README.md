# 🔐 AWS S3 Secure Storage with AWS KMS Encryption

![AWS](https://img.shields.io/badge/AWS-Cloud-orange)
![Amazon S3](https://img.shields.io/badge/Amazon%20S3-Storage-blue)
![AWS KMS](https://img.shields.io/badge/AWS-KMS-yellow)
![IAM](https://img.shields.io/badge/IAM-Security-green)

> A hands-on AWS Cloud Security lab demonstrating how to secure Amazon S3 using **AWS Key Management Service (AWS KMS)**, **IAM Least-Privilege Access Control**, **Bucket Policies**, and **AWS CLI** validation.

---

## 📖 Project Overview

This project demonstrates the implementation of a secure cloud storage solution using Amazon Web Services (AWS). The lab focuses on protecting sensitive data stored in an Amazon S3 bucket by applying multiple layers of security, including encryption, identity-based access control, and resource-based access control.

A customer-managed AWS Key Management Service (AWS KMS) key was created and configured as the default encryption mechanism for the S3 bucket using **Server-Side Encryption with AWS KMS (SSE-KMS)**. Two IAM users (**Alice** and **Bob**) were created to validate authorized and unauthorized access scenarios.

The project includes practical testing through both the **AWS Management Console** and the **AWS Command Line Interface (AWS CLI)**. The authorized user (Alice) successfully uploaded, listed, and downloaded encrypted objects, while the unauthorized user (Bob) was denied access through IAM policies, bucket policies, and AWS KMS permissions.

This repository contains the implementation steps, supporting screenshots, and the complete lab report documenting the project.

---

## 🎯 Project Objectives

- Create a secure Amazon S3 bucket.
- Encrypt stored data using a customer-managed AWS KMS key.
- Configure Server-Side Encryption (SSE-KMS).
- Implement least-privilege IAM access control.
- Create IAM users for authorized and unauthorized testing.
- Apply resource-based bucket policies.
- Configure AWS CLI for programmatic access.
- Validate successful and unsuccessful access scenarios.
- Demonstrate a defense-in-depth cloud security model.

---

## ☁️ AWS Services Used

| AWS Service | Purpose |
|-------------|---------|
| **Amazon S3** | Secure object storage for encrypted files |
| **AWS IAM** | Identity and Access Management for user authentication and authorization |
| **AWS KMS** | Customer-managed encryption keys for protecting data at rest |
| **AWS CLI** | Command-line interface for programmatic access validation |
| **IAM Policies** | Grant least-privilege permissions to authorized users |
| **Bucket Policies** | Enforce resource-level access control for the S3 bucket |

---

## 🏗️ Solution Architecture

```text
                           AWS Administrator
                                  │
                                  ▼
                      Create Amazon S3 Bucket
                                  │
                                  ▼
                  Create Customer-Managed KMS Key
                                  │
                                  ▼
              Enable Default Encryption (SSE-KMS)
                                  │
                                  ▼
                    Create IAM Users (Alice & Bob)
                                  │
                                  ▼
               Create & Attach IAM Policy to Alice
                                  │
                                  ▼
                    Apply S3 Bucket Policy
                                  │
                ┌─────────────────┴─────────────────┐
                ▼                                   ▼
      Alice (Authorized User)             Bob (Unauthorized User)
                │                                   │
                ▼                                   ▼
      Upload / Download Objects         Access Denied
      AWS Console & AWS CLI             IAM + Bucket Policy + KMS
```

---

## 🔒 Security Controls Implemented

The following AWS security controls were implemented during this lab:

- ✅ Customer-managed AWS KMS key
- ✅ Server-Side Encryption using AWS KMS (SSE-KMS)
- ✅ IAM Least-Privilege Policy
- ✅ Resource-based S3 Bucket Policy
- ✅ Separate IAM users for authorization testing
- ✅ AWS CLI authentication
- ✅ Encryption at rest
- ✅ Defense-in-depth security model
- ✅ Console and CLI permission validation

---

## 🛠️ Implementation Workflow

The following implementation sequence was performed during this lab:

1. Created an Amazon S3 bucket (`suraj-secure-data`) in the **Asia Pacific (Mumbai)** region.
2. Created a **Customer-Managed AWS KMS Key**.
3. Configured **Server-Side Encryption using AWS KMS (SSE-KMS)** as the default bucket encryption.
4. Created two IAM users:
   - **Alice** (Authorized User)
   - **Bob** (Unauthorized User)
5. Created a custom IAM policy following the **Principle of Least Privilege**.
6. Attached the custom IAM policy to Alice.
7. Enabled AWS Management Console access for both IAM users.
8. Configured an Amazon S3 Bucket Policy to restrict object access.
9. Configured AWS CLI for Alice and Bob.
10. Verified authorized access using Alice.
11. Verified unauthorized access using Bob.
12. Validated that IAM policies, Bucket Policies, and AWS KMS worked together to secure the encrypted bucket.

---

## 📂 Repository Structure

```text
aws-s3-kms-secure-storage-lab/
│
├── README.md
│
├── report/
│   └── AWS_S3_KMS_Cloud_Security_Lab_Report.pdf
│
├── images/
│   ├── (All project screenshots)

```

---

## 🧠 Skills Demonstrated

This project demonstrates practical experience with:

- Amazon S3
- AWS Identity and Access Management (IAM)
- AWS Key Management Service (AWS KMS)
- Server-Side Encryption (SSE-KMS)
- IAM Policies
- S3 Bucket Policies
- AWS CLI
- Access Control
- Cloud Data Protection
- Defense-in-Depth Security
- Principle of Least Privilege
- Security Validation and Troubleshooting

---

## 📸 Project Screenshots

The complete implementation is documented with step-by-step screenshots in the **images/** directory.

Some key stages include:

- Amazon S3 Bucket Creation
- AWS KMS Key Creation
- SSE-KMS Default Encryption
- IAM Policy Creation
- IAM Policy Attachment
- Bucket Policy Configuration
- AWS CLI Configuration
- Authorized Access Validation (Alice)
- Unauthorized Access Validation (Bob)

> 📁 All screenshots are available in the **images/** folder.

---

## 📄 Lab Report

A detailed implementation report with explanations, screenshots, security validation, and learning outcomes is available in the **report/** folder.

**Report includes:**

- Executive Summary
- Step-by-Step Implementation
- AWS Services Used
- IAM & Bucket Policy Configuration
- AWS CLI Validation
- Security Validation
- Challenges & Troubleshooting
- Learning Outcomes
- References

---

## 🎓 Key Learning Outcomes

Through this project, I gained practical experience in:

- Creating and managing Amazon S3 buckets.
- Implementing encryption using AWS KMS.
- Configuring Server-Side Encryption (SSE-KMS).
- Creating and managing IAM users.
- Applying least-privilege IAM policies.
- Creating resource-based S3 bucket policies.
- Configuring AWS CLI for programmatic access.
- Performing authorization and access validation.
- Troubleshooting AWS IAM and KMS permission issues.
- Applying defense-in-depth security principles.

---

## 🚀 Future Improvements

Potential enhancements for this project include:

- Enable Amazon S3 Versioning.
- Configure AWS CloudTrail for audit logging.
- Enable Amazon S3 Server Access Logging.
- Integrate Amazon CloudWatch monitoring and alerts.
- Implement IAM roles for application access instead of long-term access keys.
- Automate the deployment using AWS CloudFormation or Terraform.

---

## ✅ Project Summary

This project successfully demonstrates how Amazon S3, AWS IAM, AWS KMS, Bucket Policies, and AWS CLI can be combined to build a secure cloud storage solution following AWS security best practices and the Principle of Least Privilege.

## 👨‍💻 Author

**Suraj Somkuwar**

Cloud Security | AWS | Cybersecurity Enthusiast

This project was completed as part of a hands-on AWS Cloud Security laboratory focused on securing Amazon S3 using AWS KMS, IAM, Bucket Policies, and AWS CLI validation.
