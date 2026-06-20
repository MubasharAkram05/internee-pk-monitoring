# 📊 Internee.pk Cloud Monitoring and Log Analysis

## 📌 Project Overview
Implemented real-time cloud infrastructure monitoring for the 
Internee.pk system using AWS CloudWatch, including custom dashboards, 
performance metrics tracking, and automated alerting for system 
failures.

> **Objective:** Monitor the Internee.pk system for performance 
> and security using AWS CloudWatch.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| AWS CloudWatch | Metrics monitoring & dashboards |
| Amazon EC2 | Monitored compute instance |
| Amazon SNS | Email alert notifications |
| AWS IAM | Secure role-based agent access |
| CloudWatch Agent | Custom logs & metrics collection |

---

## ⚙️ Setup Steps

1. ✅ Launched EC2 instance (`internee-monitoring-server`) with 
   Ubuntu 22.04, t2.micro (Free Tier)
2. ✅ Enabled **Detailed Monitoring** on the instance (1-minute metric interval)
3. ✅ Created a custom CloudWatch Dashboard — `Internee-Monitoring-Dashboard`
4. ✅ Added widgets to track:
   - CPU Utilization
   - Network In / Network Out
   - Disk Read / Write Operations
   - Status Check Failures
5. ✅ Created an SNS Topic (`internee-alerts`) and confirmed email subscription
6. ✅ Configured CloudWatch Alarms:
   - **High-CPU-Alert** — triggers when CPU > 70% for 5 minutes
   - **Instance-Health-Alert** — triggers on instance status check failure
7. ✅ Created IAM Role (`EC2-CloudWatch-Role`) with `CloudWatchAgentServerPolicy`
8. ✅ Installed & attached CloudWatch Agent on EC2 for extended logging

---

## 🚨 Alarms Configured

| Alarm Name | Metric | Condition | Notification |
|---|---|---|---|
| High-CPU-Alert | CPUUtilization | > 70% for 5 min | Email via SNS |
| Instance-Health-Alert | StatusCheckFailed | > 0 for 5 min | Email via SNS |

---

## 📈 Metrics Tracked

- **CPU Utilization** — Tracks compute load on the instance
- **Network In/Out** — Monitors incoming/outgoing traffic
- **Disk Read/Write Ops** — Tracks storage I/O performance
- **Status Check Failed** — Detects instance/system health issues

---

## 📸 Screenshots

### 1. CloudWatch Dashboard with Widgets
<img width="1408" height="768" alt="1-CloudWatch Dashboard with widgets" src="https://github.com/user-attachments/assets/7f6bcb28-aca7-4202-8e63-af8b444fc347" />


### 2. CPU Utilization Graph
<img width="1408" height="768" alt="2-CPU Utilization graph" src="https://github.com/user-attachments/assets/40a2f166-4f59-4457-8db1-c54608a7ac34" />


### 3. Alarms List — Both Alarms Active
<img width="1280" height="564" alt="3-Alarms list (2 alarms created)" src="https://github.com/user-attachments/assets/ef83d02f-9c83-423f-8929-9528c623043a" />



### 4. SNS Email Subscription Confirmation
<img width="1408" height="740" alt="4-SNS email confirmation" src="https://github.com/user-attachments/assets/5071dda0-bf98-46a1-a425-0ab1ea97f234" />



### 5. EC2 Instance with Monitoring Enabled

<img width="1408" height="768" alt="5-EC2 instance with monitoring enabled" src="https://github.com/user-attachments/assets/5a08cbcc-7d36-4d42-8304-0038d527c1e2" />


---


## 👨‍💻 Author

**Mubashar Akram**  
Internee @ Internee.pk  
GitHub: [@MubasharAkram05](https://github.com/MubasharAkram05)
