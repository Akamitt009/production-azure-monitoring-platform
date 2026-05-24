# 📊 Production-Ready Azure VM Monitoring & Observability Platform

![Azure](https://img.shields.io/badge/Azure-Cloud-0078D4?logo=microsoftazure&logoColor=white)
![Azure Monitor](https://img.shields.io/badge/Azure-Monitor-0078D4)
![Log Analytics](https://img.shields.io/badge/Log_Analytics-KQL-68217A)
![KQL](https://img.shields.io/badge/KQL-Observability-0078D4)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Linux-E95420?logo=ubuntu)
![NGINX](https://img.shields.io/badge/NGINX-Web_Server-009639?logo=nginx)
![Azure Alerts](https://img.shields.io/badge/Azure-Alerts-red)
![Azure Workbooks](https://img.shields.io/badge/Azure-Workbooks-blue)

Production-grade Azure monitoring and observability platform implementing infrastructure telemetry, operational visibility, KQL analytics, automated alerting and cloud monitoring workflows aligned with modern DevOps and SRE operational practices.

---

# 📌 Executive Summary

Designed and implemented enterprise cloud observability platform using:

✅ Azure Monitor

✅ Azure Alerts

✅ Azure Log Analytics Workspace

✅ Azure Workbooks

✅ Linux Infrastructure Monitoring

✅ Kusto Query Language (KQL)

✅ Automated Incident Alerting

✅ Dashboard Visualization

✅ Cost Optimization

✅ Operational Troubleshooting

---

# 🎯 Business Requirement

Modern production systems require:

❌ No infrastructure visibility

❌ Manual monitoring processes

❌ Delayed incident detection

❌ Missing telemetry collection

❌ Lack of operational dashboards

❌ Slow troubleshooting workflows

This project solves those challenges using Azure-native monitoring architecture.

---

# 🛠 Prerequisites

Before deployment ensure:

| Requirement | Details |
|-------------|----------|
| Azure Subscription | Active |
| Azure Monitor | Enabled |
| Linux VM | Ubuntu VM |
| Log Analytics Workspace | Configured |
| SSH Access | Enabled |
| Azure CLI | Installed |
| Monitoring Permissions | Monitoring Contributor |

Verify Azure CLI:

```bash
az --version
```

Authenticate Azure:

```bash
az login
```

---

# 🏗 Enterprise Monitoring Architecture

```mermaid
graph TD

User[Internet User]

VM[Ubuntu Linux VM]

LAW[Log Analytics Workspace]

Monitor[Azure Monitor]

Alert[Azure Alerts]

KQL[Kusto Query Language]

Workbook[Azure Workbooks]

Email[Email Notification]

VM --> LAW

LAW --> Monitor

Monitor --> Alert

Alert --> Email

LAW --> KQL

KQL --> Workbook

VM --> Monitor

```

---

# ⚙️ Core Monitoring Components

### 📊 Azure Monitor

Centralized monitoring platform.

Capabilities:

✅ CPU Monitoring

✅ Metric Collection

✅ VM Insights

✅ Performance Visibility

---

### 📑 Log Analytics Workspace

Centralized telemetry ingestion.

Capabilities:

✅ Log Collection

✅ Infrastructure Analytics

✅ Query Processing

✅ Data Correlation

---

### 🚨 Azure Alerts

Incident detection system.

Capabilities:

✅ Automated Alerting

✅ Threshold Validation

✅ Notification Automation

---

### 📈 Azure Workbooks

Visualization platform.

Capabilities:

✅ Dashboard Creation

✅ Operational Visibility

✅ Interactive Analytics

---

### 🔍 KQL Analytics

Query engine implementation.

Capabilities:

✅ Infrastructure Queries

✅ Performance Analysis

✅ Heartbeat Monitoring

---

# ⚙️ Configuration Variables

| Variable | Description | Example |
| :--- | :--- | :--- |
| vm_name | Linux VM Name | monitoring-vm |
| cpu_threshold | CPU Alert Threshold | 70 |
| region | Azure Region | East US |
| retention_days | Log Retention | 30 |
| workspace_name | LAW Name | prod-law |

---

# ⚙️ Technology Stack

| Technology | Purpose |
|---|---|
| Azure VM | Infrastructure |
| Ubuntu Linux | Operating System |
| NGINX | Web Layer |
| Azure Monitor | Monitoring |
| Azure Alerts | Incident Response |
| Log Analytics | Telemetry Platform |
| Azure Workbooks | Dashboard Visualization |
| KQL | Query Engine |
| SSH | Linux Access |

---

# 🚀 Infrastructure Setup

### Linux VM Deployment

Created:

✅ Ubuntu Linux VM

✅ Public IP

✅ NSG Rules

✅ SSH Authentication

Hosted:

NGINX Web Application

---

# 📈 Enterprise Monitoring Implementation

## Azure Monitor

Configured:

- Azure Monitor

- VM Insights

- Metrics Collection

- Performance Analytics

---

## CPU Monitoring

Configured:

- Percentage CPU

- Real-Time Metrics

- Performance Visualization

---

# 🚨 Incident Alerting Platform

Alert Configuration:

| Configuration | Value |
|---|---|
| Alert Type | Metric Alert |
| Metric | Percentage CPU |
| Threshold | >70% |
| Severity | Sev2 |
| Notification | Email |
| Evaluation | Real Time |

---

# 🔥 Incident Simulation

Stress utility:

```bash
sudo apt update

sudo apt install stress -y

stress --cpu 4 --timeout 600
```

Validated:

✅ CPU Spike Detection

✅ Alert Trigger

✅ Email Notification

✅ Dashboard Update

---

# 📑 KQL Queries

## CPU Monitoring Query

```kql
InsightsMetrics

| where Namespace=="Processor"

| summarize AvgCPU=avg(Val)

by bin(TimeGenerated,5m)

| render timechart
```

---

## Heartbeat Monitoring

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

# 📸 Project Proof Screenshots

## VM Monitoring Dashboard

![VM Monitoring Dashboard](images/vm-monitoring-dashboard.PNG)

---

## Network Monitoring Dashboard

![Network Monitoring](images/network-monitoring-dashboard.PNG)

---

## Disk Monitoring Dashboard

![Disk Monitoring](images/disk-monitoring-dashboard.PNG)

---

## Azure Monitor Onboarding

![Azure Monitor](images/azure-monitor-onboarding.PNG)

---

## CPU Alert Rule

![CPU Alert](images/cpu-alert-rule-configuration.PNG)

---

## Email Action Group

![Action Group](images/email-action-group-configuration.PNG)

---

## Alert Review

![Alert Review](images/alert-rule-review.PNG)

---

## Alerts Dashboard

![Alerts](images/alerts-dashboard.PNG)

---

## Email Notification

![Email Notification](images/email-alert-notification.PNG)

---

## Email Notification Validation

![Email Validation](images/email-alert-notification-2.PNG)

---

## Heartbeat Query

![Heartbeat](images/heartbeat-kql-query.PNG)

---

## Heartbeat Results

![Heartbeat Results](images/heartbeat-monitoring-results.PNG)

---

## CPU Stress Validation

![CPU Stress](images/linux-cpu-stress-testing.PNG)

---

## Deployment Validation

![Deployment Complete](images/monitoring-deployment-complete.PNG)

---

# ⚠️ Engineering Challenges Solved

| Challenge | Solution |
|---|---|
| SSH Failure | Native SSH + PEM |
| Alerts Not Triggering | Stress Utility |
| Missing Logs | AMA Validation |
| Cost Increase | Bastion Removal |

---

# 🧠 Skills Demonstrated

Azure Monitor

Azure Alerts

KQL

Azure Workbooks

Cloud Monitoring

Incident Engineering

Linux Administration

Infrastructure Monitoring

Operational Visibility

Dashboard Engineering

Cloud Operations

Observability Engineering

---

# 📈 Business Outcome

Successfully implemented cloud-native observability platform supporting:

✅ Infrastructure Monitoring

✅ Incident Detection

✅ Alert Engineering

✅ Linux Visibility

✅ Dashboard Visualization

✅ Operational Troubleshooting

---

# 👨‍💻 Author

## Amit Kumar

Cloud Engineer | Azure Administrator | Observability Engineer

GitHub

https://github.com/Akamitt009

LinkedIn

https://www.linkedin.com/in/amit-kumar-657255232/
