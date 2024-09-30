## AWS CloudFormation Overview
- **Infrastructure as Code (IaC)**: CloudFormation enables you to define and provision AWS infrastructure using **templates** (in JSON or YAML).
- **Stack**: A **stack** is a collection of AWS resources that you manage as a single unit. You create, update, or delete a stack based on the template.
- **Template**: A **CloudFormation template** defines the resources and their configurations. It includes **resources**, **parameters**, **mappings**, **outputs**, and **conditions**.
- **StackSet**: Allows you to deploy CloudFormation stacks across multiple AWS accounts and regions.

## Key Features
- **Automated Provisioning**: CloudFormation automates the provisioning of resources, ensuring consistency and reducing manual steps.
- **Declarative Syntax**: You describe what resources you want (not how to create them), and CloudFormation takes care of the orchestration.
- **Rollback on Failure**: If stack creation or update fails, CloudFormation automatically rolls back to the previous known good state.
- **Change Sets**: Preview how proposed changes will affect your existing stack before applying updates.
- **Cross-Stack References**: Share outputs from one stack with another stack using **Exports** and **Imports**.

## Use Cases
- **Multi-tier Applications**: Define and deploy complex architectures (e.g., web servers, databases, load balancers) in a repeatable and consistent manner.
- **Compliance and Governance**: Enforce compliance by using version-controlled templates to deploy standardized infrastructure.
- **Disaster Recovery**: Quickly redeploy infrastructure in another region using the same CloudFormation template.

## Key Concepts for the Exam
- **Parameters**: Allow you to pass values into the template at runtime, making your templates more dynamic.
- **Outputs**: Return values from your CloudFormation stack, such as resource IDs or endpoint URLs, which can be used in other stacks or displayed after stack creation.
- **Mappings**: Static key-value pairs in the template, useful for creating conditional resource definitions (e.g., AMI IDs per region).
- **Conditions**: Define whether certain resources are created or configured based on input parameters or environmental conditions.
- **Drift Detection**: Detects if any resources have been manually changed outside of CloudFormation, ensuring your stack remains in sync with the template.

## Permissions
- **IAM Roles**: CloudFormation uses IAM roles to create, update, or delete resources on your behalf.
- **Stack Policies**: Used to prevent certain resources in a stack from being unintentionally updated or deleted during stack updates.

## Common Exam Topics
- **Template Structure**: Know the key sections of a CloudFormation template (`Resources`, `Parameters`, `Outputs`, `Conditions`, etc.).
- **Stack Creation and Updates**: Understand how stacks are created and updated, including the use of **Change Sets**.
- **IAM Role Permissions**: How CloudFormation interacts with IAM and permissions to create resources.
- **Rollback**: What happens during stack failures and how rollback occurs.
- **Cross-Stack References**: Using outputs from one stack in another.

## Common Exam Questions
- How to manage **stack updates** and handle **rollback** in case of failure?
- When to use **parameters**, **mappings**, **conditions**, and **outputs** in a template?
- How to share **resources** between CloudFormation stacks?
