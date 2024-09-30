## Amazon EventBridge Overview
- **Event Bus**: Central entity that receives, routes, and processes events.
- **Event Source**: AWS services (e.g., EC2, Lambda, S3), custom applications, or SaaS providers can send events.
- **Rules**: Match events based on patterns, then route matched events to **targets** (like Lambda, SQS, Step Functions).
  - A single rule can route an event to **multiple targets**.
- **Event Targets**: AWS services (e.g., Lambda, Step Functions, SNS, SQS, etc.).
- **Dead Letter Queue (DLQ)**: If a target fails to receive an event, it can be sent to a **DLQ** for further analysis.
- **Schemas**: EventBridge can automatically detect and generate schemas for events.
- **EventBus Types**:
  1. **Default Event Bus**: Receives events from AWS services.
  2. **Custom Event Bus**: For custom applications or SaaS events.
  3. **Partner Event Bus**: For SaaS integrations.

## Key Features
- **Event Pattern Matching**: Filters and processes events based on attributes or conditions (e.g., source, detail).
- **Event Delivery**: Events are **asynchronously** delivered to targets.
- **Scheduling**: EventBridge rules can be triggered on a **schedule** (e.g., cron expressions).
- **High Availability**: EventBridge is fully managed and scales automatically.

## Use Cases
- **Serverless Event-Driven Applications**: Trigger Lambda functions in response to events.
- **Cross-Service Automation**: Automate workflows across AWS services (e.g., EC2 state change → SNS).
- **Integration with SaaS**: Use EventBridge to integrate with external SaaS providers.

## Key Limits
- **5 targets per rule** (can fan out to more using SNS/SQS).
- **64 KB size limit** for each event payload.

## Permissions
- **IAM Role Permissions**: EventBridge must have permissions to invoke target services.

## Key Concepts for Exam
- **Rule Evaluation**: Rules are **always evaluated**, but only matched events are routed to targets.
- **DLQs**: Important for handling failures in event delivery.
- **Use Cases for EventBridge vs SQS, SNS**:
  - **EventBridge**: Routing based on event patterns, event-driven architectures.
  - **SQS**: Message queuing (decoupling systems).
  - **SNS**: Pub/Sub model (broadcast to multiple subscribers).