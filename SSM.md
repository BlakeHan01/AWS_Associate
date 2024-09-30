## AWS Systems Manager (SSM) Overview
AWS Systems Manager provides a unified interface to view and manage your AWS resources and automate operational tasks across AWS services.

### Key Components

### 1. **SSM Session Manager**
- **Purpose**: Securely manage and access your EC2 instances without needing an SSH or RDP connection, VPN, or open inbound ports.
- **Key Features**:
  - Secure, browser-based or CLI access to EC2 instances.
  - No need for SSH keys or bastion hosts.
  - Supports logging all session activity to **CloudWatch** or **S3** for auditing.
- **Use Cases**:
  - Managing instances in private subnets.
  - Auditing and compliance for instance access.

### 2. **Run Command**
- **Purpose**: Run remote commands across a fleet of EC2 instances or on-premises servers without logging into them.
- **Key Features**:
  - Execute shell scripts, PowerShell commands, or SSM documents (automation scripts).
  - Centrally manage and audit commands with **CloudWatch Logs** or **S3**.
  - No need to open SSH or RDP access.
- **Use Cases**:
  - Automating administrative tasks (e.g., installing software, patching, updates).
  - Orchestrating complex operations across multiple instances.

### 3. **Patch Manager**
- **Purpose**: Automate patching of operating systems and applications on your EC2 instances or on-premises servers.
- **Key Features**:
  - Schedule automated patching using **maintenance windows**.
  - Supports both security patches and non-security updates.
  - Integration with **Amazon Inspector** to assess vulnerabilities.
- **Use Cases**:
  - Ensure compliance with security patching requirements.
  - Automatically patch instances without downtime during maintenance windows.

### 4. **Maintenance Windows**
- **Purpose**: Schedule regular, recurring operational tasks (e.g., patching, running scripts) during predefined time windows.
- **Key Features**:
  - Automate operational tasks during off-hours.
  - Integrates with **Run Command**, **Patch Manager**, and **Automation**.
  - Control the number of tasks running concurrently.
- **Use Cases**:
  - Scheduling patching, backups, or compliance checks during low-traffic periods.
  - Orchestrating updates and operational tasks in a controlled manner.

### 5. **Automation**
- **Purpose**: Automate common operational tasks such as creating or updating resources using predefined or custom workflows.
- **Key Features**:
  - Predefined automation documents (e.g., AMI creation, instance start/stop).
  - Integrates with AWS services like **CloudWatch Events** and **EventBridge** for triggering automations.
  - Track progress and audit tasks.
- **Use Cases**:
  - Automatically remediate issues (e.g., restarting unhealthy instances).
  - AMI creation and updates.
  - Automating repetitive tasks like resource provisioning or updates.

### Permissions
- Managed via **IAM policies** for granular control over who can access and execute SSM tasks.
- Session Manager can restrict users to specific instances or commands using **IAM role permissions**.

### Common Exam Topics
- Secure access to EC2 instances using **SSM Session Manager** without SSH.
- Automating patch management across fleets with **Patch Manager**.
- Scheduling recurring tasks using **Maintenance Windows**.
- Running commands or scripts across EC2 instances with **Run Command**.
- Automating operational workflows with **SSM Automation**.

### Common Exam Questions
- How to access EC2 instances in private subnets without opening inbound ports?
- How to automate OS patching for compliance using **Patch Manager**?
- When to use **Run Command** versus **Automation** for remote management tasks?
