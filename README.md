# Production-Ready Azure VM Monitoring & Observability Platform

## Executive Summary

Designed and implemented a production-style cloud monitoring and observability platform on Microsoft Azure using Linux virtual machines, Azure Monitor, Log Analytics Workspace, Kusto Query Language (KQL), Azure Alerts, and Azure Workbooks.

This project demonstrates real-world cloud operations practices including:

* Infrastructure monitoring
* Incident alerting
* Operational visibility
* Performance analysis
* Linux service monitoring
* Dashboard visualization
* Cost optimization
* Production troubleshooting

The environment simulates a modern DevOps/SRE monitoring workflow where infrastructure metrics, logs, and operational events are continuously collected, analyzed, visualized, and used to trigger automated notifications.

---

# Architecture

```text
Internet Users
       |
       v
Azure Public IP
       |
       v
Ubuntu Linux VM (NGINX)
       |
       +----------------+
       |                |
       v                v
Azure Monitor      Log Analytics Workspace
       |                |
       +----------------+
                |
                v
        Azure Alerts + KQL Queries
                |
                v
         Email Notifications
                |
                v
         Azure Workbooks Dashboard
```

---

# Technologies Used

| Service                 | Purpose                   |
| ----------------------- | ------------------------- |
| Microsoft Azure         | Cloud Platform            |
| Azure VM                | Linux server hosting      |
| Ubuntu 24.04            | Operating System          |
| NGINX                   | Web server                |
| Azure Monitor           | Infrastructure monitoring |
| Log Analytics Workspace | Log storage and analytics |
| Azure Alerts            | Incident alerting         |
| Azure Workbooks         | Dashboard visualization   |
| KQL                     | Querying monitoring logs  |
| SSH                     | Secure Linux access       |

---

# Core Implementation Areas

## Infrastructure Setup

* Created Azure Ubuntu Linux Virtual Machine
* Configured Public IP access
* Configured NSG firewall rules
* Connected using SSH PEM key authentication
* Hosted live web application on VM

---

# Enterprise Monitoring & Observability

## Azure Monitor

* Enabled Azure Monitor for VM
* Connected VM with Log Analytics Workspace
* Enabled VM Insights
* Collected performance metrics

## CPU Monitoring

Configured CPU monitoring using:

* Percentage CPU metrics
* Azure Monitor metrics
* Real-time CPU visualization

---

# Incident Alerting & Response System

Created production-style CPU alerts:

| Configuration | Value              |
| ------------- | ------------------ |
| Alert Type    | Metric Alert       |
| Metric        | Percentage CPU     |
| Threshold     | > 70%              |
| Severity      | Sev2               |
| Action Group  | Email Notification |
| Evaluation    | Real-time          |

---

# Incident Simulation

Used Linux stress utility to simulate high CPU load:

```bash
sudo apt update
sudo apt install stress -y
stress --cpu 4 --timeout 600
```

This generated:

* High CPU spikes
* Azure Monitor alerts
* Email notifications
* Monitoring dashboard metrics

---

# Email Notification Proof

Successfully configured:

* Azure Alert Action Group
* Email notification delivery
* Real-time alert emails

Example:

```text
Alert Name: High-CPU-Alert
Metric: Percentage CPU
Threshold: Greater than 70%
Severity: Sev2
```

---

# Log Analytics & KQL

## CPU Monitoring Query

```kql
InsightsMetrics
| where Namespace == "Processor"
| summarize AvgCPU=avg(Val) by bin(TimeGenerated, 5m)
| render timechart
```

---

## Heartbeat Monitoring Query

```kql
Heartbeat
| sort by TimeGenerated desc
| take 10
```

---

## Syslog Query

```kql
Syslog
| sort by TimeGenerated desc
| take 50
```

---

# Workbook Dashboard

Created Azure Workbook dashboard for:

* CPU visualization
* Time-series monitoring
* Infrastructure observability
* Operational insights

Dashboard includes:

* Interactive charts
* Real-time metrics
* VM monitoring visualization

---

# Linux Operations Performed

## SSH Access

```bash
ssh -i "C:\Users\Amit Sharma\Downloads\amit009.pem" azureuser@4.213.35.81
```

---

## NGINX Installation

```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

## NGINX Status Monitoring

```bash
sudo systemctl status nginx
```

---

# Technical Challenges & Engineering Solutions

## Challenge 1 — SSH Connection Failure

### Problem

Initial SSH connection through Azure Bastion failed.

### Solution

* Used Native SSH
* Connected using PEM private key
* Verified NSG port 22 access

---

## Challenge 2 — Alerts Not Triggering

### Problem

CPU alerts were not firing initially.

### Solution

* Installed stress utility
* Generated artificial CPU load
* Increased CPU consumption manually
* Verified Azure Monitor metrics

---

## Challenge 3 — No Logs Appearing in Log Analytics

### Problem

Syslog/KQL queries initially returned no data.

### Solution

* Verified Azure Monitor Agent heartbeat
* Used correct KQL tables
* Queried Heartbeat and InsightsMetrics tables
* Adjusted time range

---

## Challenge 4 — Cost Optimization

### Problem

Azure Bastion was increasing Pay-As-You-Go cost.

### Solution

* Deleted Azure Bastion resource
* Continued using SSH PEM authentication
* Reduced monitoring lab cost significantly

---

# Technical Competencies Demonstrated

## Azure Skills

* Azure VM Management
* Azure Monitor
* Azure Alerts
* Azure Workbooks
* Log Analytics
* Infrastructure Monitoring
* Incident Monitoring
* Cloud Operations

---

## Linux Skills

* SSH Administration
* Linux Monitoring
* NGINX Administration
* Service Management
* CPU Stress Testing
* Operational Troubleshooting

---

## Observability Skills

* KQL Querying
* Metrics Analysis
* Alert Engineering
* Dashboard Visualization
* Operational Visibility
* Performance Monitoring

---

# Live Services

## Live Website

```text
http://4.213.35.81
```

---

# Screenshots

## VM Monitoring Dashboard

![VM Monitoring Dashboard](images/vm-monitoring-dashboard.PNG)

## Network Monitoring Dashboard

![Network Monitoring Dashboard](images/network-monitoring-dashboard.PNG)

## Disk Monitoring Dashboard

![Disk Monitoring Dashboard](images/disk-monitoring-dashboard.PNG)

## Azure Monitor Onboarding

![Azure Monitor Onboarding](images/azure-monitor-onboarding.PNG)

## CPU Alert Rule Configuration

![CPU Alert Rule Configuration](images/cpu-alert-rule-configuration.PNG)

## Email Action Group Configuration

![Email Action Group Configuration](images/email-action-group-configuration.PNG)

## Alert Rule Review

![Alert Rule Review](images/alert-rule-review.PNG)

## Alerts Dashboard

![Alerts Dashboard](images/alerts-dashboard.PNG)

## Email Alert Notification

![Email Alert Notification](images/email-alert-notification.PNG)

## Email Alert Notification 2

![Email Alert Notification 2](images/email-alert-notification-2.PNG)

## Heartbeat KQL Query

![Heartbeat KQL Query](images/heartbeat-kql-query.PNG)

## Heartbeat Monitoring Results

![Heartbeat Monitoring Results](images/heartbeat-monitoring-results.PNG)

## Linux CPU Stress Testing

![Linux CPU Stress Testing](images/linux-cpu-stress-testing.PNG)

## Monitoring Deployment Complete

![Monitoring Deployment Complete](images/monitoring-deployment-complete.PNG)

---

# Business & Technical Outcome

Successfully implemented a cloud-native monitoring and observability solution capable of:

* Detecting infrastructure incidents
* Sending automated alerts
* Monitoring Linux VM health
* Visualizing operational metrics
* Performing production-style infrastructure monitoring

---

# Professional Project Summary

```text
Engineered a production-grade Azure monitoring and observability platform using Azure Virtual Machines, Azure Monitor, Log Analytics Workspace, Azure Alerts, Kusto Query Language (KQL), and Azure Workbooks. Implemented real-time CPU monitoring, automated incident alerting via email notifications, Linux operational monitoring, dashboard visualization, and infrastructure observability workflows aligned with DevOps and SRE operational practices.
```

---

# Author

Amit Kumar

GitHub:
[https://github.com/Akamitt009](https://github.com/Akamitt009)

## LinkedIn
https://www.linkedin.com/in/amit-kumar-657255232/
