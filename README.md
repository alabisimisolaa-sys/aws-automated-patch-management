# Multi-OS Patch Management with AWS Systems Manager (SSM)

## Project Overview
This project demonstrates the implementation of an automated patching solution to maintain 100% security compliance across a hybrid fleet of **Amazon Linux 2** and **Windows Server 2019** instances. By leveraging AWS Systems Manager (SSM) Patch Manager, I eliminated manual update processes and ensured a consistent security posture across multiple environments.

## Key Achievements
* **Custom Security Baselines:** Architected a specific patch baseline for Windows Server 2019 to automate the approval of `Critical` and `Important` security updates with a 3-day approval delay.
* **Tag-Based Governance:** Implemented a scalable tagging strategy (`Patch Group: LinuxProd` and `WindowsProd`) to target specific workloads without affecting unrelated infrastructure.
* **Fleet-Wide Automation:** Successfully executed simultaneous "Scan and Install" operations across 6 managed nodes using the `AWS-RunPatchBaseline` SSM document.
* **Compliance Verified:** Achieved a "Compliant" status for the entire fleet, monitored through the centralized SSM Compliance Dashboard.

## Tech Stack
* **Cloud Provider:** Amazon Web Services (AWS)
* **Core Service:** Systems Manager (SSM) - Patch Manager, Fleet Manager, State Manager
* **Infrastructure:** EC2 (Linux & Windows Server), IAM (Service Roles)

## Implementation Steps
1. **Targeting:** Assigned instances to specific Patch Groups using EC2 Tags.
2. **Configuration:** Defined custom approval rules for Windows and utilized default baselines for Linux.
3. **Execution:** Triggered on-demand patching operations via SSM Run Command.
4. **Audit:** Verified remediation through the Patch Manager Dashboard and Compliance Reporting.

---
*This project was completed as part of a hands-on lab focused on Cloud Infrastructure hardening and Systems Management.*
