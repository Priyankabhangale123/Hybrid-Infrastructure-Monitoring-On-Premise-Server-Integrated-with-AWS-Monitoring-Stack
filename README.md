# Hybrid-Infrastructure-Monitoring-On-Premise-Server-Integrated-with-AWS-Monitoring-Stack

Designed and implemented a hybrid monitoring solution by integrating an on-premise virtual machine with AWS CloudWatch using the CloudWatch Agent. Built centralized dashboards and configured real-time alerting using SNS to monitor both cloud and on-prem environments efficiently.

## Project Overview
This project showcases a Hybrid Monitoring System where an on-premise server (Virtual Machine) is connected with AWS CloudWatch for unified monitoring.

The solution gathers metrics from:
* AWS EC2 Instance
* On-Premise Virtual Machine
All metrics are visualized in a single CloudWatch dashboard, along with automated alerting through SNS notifications.

<img width="864" height="510" alt="image" src="https://github.com/user-attachments/assets/ec0d05c7-f3bb-4b78-931a-5ff1233f3b09" />


## Architecture
On-Prem VM → CloudWatch Agent → AWS CloudWatch
↓
EC2 Instance → Metrics → Dashboard + Alarms → SNS (Email Alerts)

## Technologies Used
* AWS CloudWatch
* AWS EC2
* AWS SNS
* IAM Roles & Policies
* Ubuntu (Virtual Machine)
* CloudWatch Agent

## Implementation Steps
## 1. On-Premise VM Setup
Created an Ubuntu VM using VirtualBox
Installed and configured CloudWatch Agent

<img width="838" height="418" alt="image" src="https://github.com/user-attachments/assets/3832f7a8-401e-4146-bce8-4634de3f9870" />

<img width="1600" height="811" alt="image" src="https://github.com/user-attachments/assets/8274301a-ebd7-40ed-badf-48682e44ba5a" />

## 2. EC2 Instance Configuration
Launched an Ubuntu EC2 instance
Attached IAM Role with CloudWatch access permissions

## 3. CloudWatch Agent Setup
Configured CloudWatch Agent on both VM and EC2
Metrics collected:

* CPU utilization
* Memory usage
* Disk usage


<img width="1365" height="468" alt="image" src="https://github.com/user-attachments/assets/baef0eab-f6db-46c5-bdff-31e1810b6ded" />


<img width="1273" height="625" alt="Hybrid-Infrastructure-Monitoring-using-AWS-CloudWatch_README md at master · monikagaikwad22_Hybrid-Infrastructure-Monitoring-using-AWS-CloudWatch - Google Chrome 28-03-2026 23_34_29" src="https://github.com/user-attachments/assets/a3fdabba-d3fe-40bc-ada2-25d55c7cc29d" />

## 4. Agent Status Verification
Started CloudWatch Agent service
Verified successful execution


## 5. Metrics Validation
* Verified metrics in CloudWatch console
Examples:
* EC2 → CPUUtilization
* VM → mem_used_percent

  <img width="1361" height="635" alt="image" src="https://github.com/user-attachments/assets/29adaf7b-136f-4a03-bf3d-5ab8a3fc3ef3" />

## 6. Dashboard Creation
* Created a unified CloudWatch Dashboard including:
EC2 CPU metrics
VM Memory usage
VM Disk utilization

<img width="1365" height="630" alt="image" src="https://github.com/user-attachments/assets/00cdb065-9603-4ac0-b045-1338e3ef08dc" />

## 7. SNS Alert Setup
* Created SNS Topic
* Subscribed email for receiving alerts

  <img width="1920" height="1020" alt="AWS Notification - Subscription Confirmation - priyanka92004@gmail com - Gmail - Google Chrome 28-03-2026 23_43_19" src="https://github.com/user-attachments/assets/dd0f85dd-f630-414c-888a-26cb541b48f2" />

##  8. Alarm Configuration
Configured CloudWatch Alarms:

* EC2 CPU Utilization > 70%
* VM Memory Usage > 70%

## 9. Testing & Validation
Generated load using stress command
Observed:
* Metric spikes
* Alarm triggering
* Email notification received

<img width="1920" height="1020" alt="AWS Notification - Subscription Confirmation - priyanka92004@gmail com - Gmail - Google Chrome 28-03-2026 23_47_01" src="https://github.com/user-attachments/assets/aba5579c-6901-4a3f-abde-7138c35e1cd0" />

## Final Outcome
* Unified monitoring for hybrid infrastructure
* Real-time performance tracking
* Automated alerting via SNS
* Successfully validated monitoring through stress test

## Key Learnings
* Designing hybrid cloud monitoring architecture
* CloudWatch Agent setup & troubleshooting
* Custom metrics collection
* Dashboard creation & alert configuration
* Handling real-world monitoring scenarios

## Conclusion
This project demonstrates an effective approach to integrating on-premise systems with AWS CloudWatch, enabling centralized monitoring and proactive alerting across hybrid environments.







