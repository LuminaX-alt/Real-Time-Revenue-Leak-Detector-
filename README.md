# Real-Time Revenue Leak Detector (SaaS / Fintech)

A fully serverless application that detects and prevents revenue leakage in real time for SaaS and Fintech platforms. Built for the AWS Lambda Hackathon, this solution uses an event-driven architecture to monitor subscription events, billing activity, and usage logs, identifying anomalies that indicate lost or misreported revenue.

---

## 🚀 Overview

In modern subscription-based systems, even a small billing error or missed transaction can compound into significant revenue loss. This project solves that by using AWS tools—especially **AWS Lambda**—to capture, analyze, and respond to anomalies as they happen, ensuring financial integrity with zero infrastructure management.

---

## 🧠 What It Does

- Detects anomalies in real-time across usage, subscription, and billing data.
- Validates actual charges against defined pricing rules.
- Identifies silent churn, failed payment retries, or excessive usage with no charge.
- Sends alerts instantly and can trigger rollback or escalation workflows.

---

## 🛠️ Technologies Used

### Languages & Libraries
- Python (Lambda functions)
- Scikit-learn / SciPy (for anomaly scoring)
- JavaScript (optional dashboard)

### AWS Cloud Services
- **AWS Lambda** – core serverless compute engine
- **Amazon EventBridge** – event trigger source
- **Amazon DynamoDB** – stores anomalies and pricing rules
- **AWS Step Functions** – multi-step workflows
- **Amazon CloudWatch** – observability/logging
- **Amazon SNS** – real-time notifications
- **AWS IAM** – secure access control
- **AWS S3** – optional event log storage

---
How AWS Lambda Was Used
AWS Lambda is the centerpiece of this project. It is configured to run automatically in response to incoming events from Amazon EventBridge—including user activity, billing events, or webhook calls from services like Stripe or Razorpay.

Each Lambda function performs the following key actions:

Parses incoming events to extract subscription, billing, or usage data.

Compares actual charges against predefined pricing rules from Amazon DynamoDB.

Executes lightweight anomaly detection algorithms (statistical + ML-based) to detect mismatches, silent churn, or failed transactions.

Logs results to CloudWatch, stores anomaly metadata in DynamoDB, and sends alerts through Amazon SNS.

Optionally triggers Step Functions workflows for escalation or rollback.

This event-driven Lambda architecture allows the system to operate in real time with zero infrastructure overhead, making it scalable, reliable, and cost-efficient.

📌 Roadmap
Add full-featured dashboard using AWS Amplify or Vercel

Add Stripe and Razorpay webhook support out of the box

Integrate advanced ML models (e.g., Isolation Forest, LSTM)

Self-healing actions (e.g., user flagging, auto refund rollback)

Open-source template for rapid deployment in SaaS projects



![image](https://github.com/user-attachments/assets/f6e4b39d-79dd-440c-ae0b-1314b63b2714)

![image](https://github.com/user-attachments/assets/f8a72710-4d02-49b9-b73b-055f11307559)

![image](https://github.com/user-attachments/assets/22dc5c82-3cdf-45b6-8956-a679af12bb97)

![image](https://github.com/user-attachments/assets/c359a1a5-a5c5-438d-b9d8-02587f67ce08)

![image](https://github.com/user-attachments/assets/5ec2e16e-a29f-4d35-8309-96a89ce92821)

![image](https://github.com/user-attachments/assets/6408fb45-e4a3-42cb-954c-11489a28f4f6)


