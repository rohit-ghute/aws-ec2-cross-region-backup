# AWS EC2 Cross-Region Backup using AWS Backup

## Project Overview
This project demonstrates how to implement an automated EC2 backup and disaster recovery (DR) solution using AWS Backup with cross-region replication.

The solution ensures data protection and availability by copying EC2 backups from a primary AWS region to a secondary region.

---

## Architecture Summary
- Source Region: Asia Pacific (Mumbai) – ap-south-1
- Destination Region: Asia Pacific (Singapore) – ap-southeast-1
- AWS Service: AWS Backup
- Resource Protected: Amazon EC2 Instance

---

## Problem Statement
Manual EC2 backups are not reliable for disaster recovery scenarios.  
If backups are stored in the same region, a regional failure can result in data loss.

This project solves the problem by:
- Automating EC2 backups
- Replicating backups to another AWS region
- Retaining recovery points for restore operations

---

## Tools & Services Used
- Amazon EC2
- AWS Backup
- AWS Backup Vault
- AWS Backup Plan
- Amazon EBS
- Amazon AMI
- IAM (Service Role)

---

## Implementation Steps

### 1. EC2 Instance Creation
- Launched an EC2 instance in Mumbai region.
- Created sample data inside the instance to validate backup integrity.

### 2. Backup Vault Configuration
- Created a primary backup vault in the source region.
- Created a disaster recovery backup vault in the destination region.

### 3. Backup Plan Creation
- Configured a daily backup plan using AWS Backup.
- Defined backup retention policies.

### 4. Resource Assignment
- Assigned the EC2 instance to the backup plan using tags/resource assignment.

### 5. Cross-Region Backup Copy
- Enabled cross-region copy rule to replicate backups to Singapore region.

### 6. Backup Execution
- Triggered on-demand backup.
- Verified successful completion of backup job.

### 7. Recovery Validation
- Verified AMI / recovery point creation for restore readiness.

---

## Screenshots
All screenshots related to the implementation are available in the `screenshots/` directory and include:
- EC2 instance running
- Sample data inside EC2
- Backup vault creation
- Backup plan configuration
- Resource assignment
- Cross-region copy rule
- Backup job completion
- AMI recovery point

---

## Outcome
- Automated EC2 backup process
- Cross-region disaster recovery enabled
- Reduced risk of data loss
- Improved system reliability and availability

---

## Key Learnings
- AWS Backup architecture
- Disaster recovery strategies
- Cross-region replication
- EC2 backup and restore workflow

---

## Author
**Rohit Ghute**  
AWS Cloud & DevOps Engineer (Fresher)  
LinkedIn: https://www.linkedin.com/in/rohit-ghute-917b662ab/
