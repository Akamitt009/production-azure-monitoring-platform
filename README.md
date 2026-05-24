# 📊 Production-Ready Azure VM Monitoring & Observability Platform

![Azure](https://img.shields.io/badge/Azure-Cloud-0078D4?logo=microsoftazure&logoColor=white)
![Azure Monitor](https://img.shields.io/badge/Azure-Monitor-0078D4)
![Log Analytics](https://img.shields.io/badge/Log_Analytics-KQL-68217A)
![KQL](https://img.shields.io/badge/KQL-Observability-0078D4)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Linux-E95420?logo=ubuntu)
![NGINX](https://img.shields.io/badge/NGINX-Web_Server-009639?logo=nginx)
![Azure Alerts](https://img.shields.io/badge/Azure-Alerts-red)
![Azure Workbooks](https://img.shields.io/badge/Azure-Workbooks-blue)

Production-grade Azure monitoring and observability platform implementing infrastructure telemetry, operational visibility, KQL analytics, alert engineering and cloud monitoring workflows aligned with SRE and DevOps operational practices.

---

# 📌 Executive Summary

Designed and implemented enterprise cloud observability platform using:

✅ Azure Monitor

✅ Log Analytics Workspace

✅ Azure Alerts

✅ Azure Workbooks

✅ Linux Infrastructure Monitoring

✅ Kusto Query Language (KQL)

✅ Operational Visibility

✅ Dashboard Visualization

✅ Incident Detection

✅ Performance Monitoring

✅ Cost Optimization

---

# 🎯 Business Requirement

Modern production infrastructure requires:

❌ Missing telemetry visibility

❌ Delayed incident detection

❌ Manual monitoring process

❌ No operational dashboard

❌ Slow troubleshooting

❌ Missing alert automation

This project solves those challenges using Azure-native observability architecture.

---

# 🛠 Prerequisites

Ensure environment readiness.

| Requirement | Details |
|-------------|----------|
| Azure Subscription | Active |
| Azure Monitor | Enabled |
| Ubuntu Linux VM | Deployed |
| Log Analytics Workspace | Configured |
| Azure CLI | Installed |
| SSH Access | Enabled |
| Monitoring Permissions | Contributor |

Authenticate:

```bash
az login
```

Verify:

```bash
az --version
```

---

# 🏗️ Architecture Design

```mermaid
graph TD

subgraph Target_Infrastructure

AKS[Azure Kubernetes Service]

VMs[Azure Virtual Machines]

end

subgraph Data_Collection

Prom[Prometheus]

AMA[Azure Monitor Agent]

end

subgraph Storage

LAW[Log Analytics Workspace]

end

subgraph Visualization

Grafana[Grafana Dashboard]

AM[Azure Monitor Alerts]

end

AKS --> Prom

VMs --> Prom

AKS --> AMA

VMs --> AMA

AMA --> LAW

Prom --> Grafana

LAW --> AM

Grafana --> Teams

AM --> Teams

```

---

# ⚙️ Core Monitoring Components

### 📊 Azure Monitor

Capabilities:

✅ VM Monitoring

✅ Metric Collection

✅ VM Insights

✅ Infrastructure Visibility

---

### 📑 Log Analytics Workspace

Capabilities:

✅ Centralized Logging

✅ Telemetry Collection

✅ KQL Query Analytics

---

### 📈 Azure Workbooks

Capabilities:

✅ Dashboard Visualization

✅ Trend Analysis

✅ Infrastructure Analytics

---

### 🔍 KQL Analytics

Capabilities:

✅ CPU Monitoring

✅ Heartbeat Monitoring

✅ Syslog Analysis

✅ Performance Investigation

---

### 🚨 Azure Alerts

Capabilities:

✅ Automated Alerting

✅ Threshold Detection

✅ Incident Notification

---

# 🚨 Production Alerting Thresholds Built-In

🔴 High CPU Utilization

Trigger:

CPU > 85% for 5 minutes

---

🔴 High Memory Usage

Trigger:

Memory > 85%

---

🟡 Disk Space Warning

Trigger:

Disk Utilization > 85%

---

❌ Service Failure

Trigger:

Critical Service Down

---

🚨 Notification Targets

Configured:

- Email Notification
- Azure Alert Action Group
- Incident Visibility

---

# ⚙️ Configuration Variables

Modify deployment using:

terraform.tfvars

| Variable Name | Description | Default Value |
|---|---|---|
| resource_group_name | Resource Group | azure-monitoring-rg |
| location | Azure Region | East US |
| retention_in_days | Log Retention | 30 |
| workspace_name | LAW Name | prod-law |
| cpu_alert_threshold | CPU Alert Value | 85 |

---

# ⚙️ Technology Stack

| Technology | Purpose |
|---|---|
| Azure Monitor | Monitoring |
| Azure Alerts | Incident Detection |
| Log Analytics | Log Collection |
| Azure Workbooks | Dashboard |
| Ubuntu Linux | OS |
| NGINX | Web Layer |
| SSH | Access |
| KQL | Query Engine |

---

# 🚀 Infrastructure Setup

Implemented:

✅ Ubuntu Linux VM

✅ NSG Configuration

✅ Public IP

✅ SSH Access

✅ Web Application Hosting

---

# 📈 Monitoring Implementation

Configured:

### Azure Monitor

- VM Insights

- Metrics Collection

- CPU Analytics

---

### Log Analytics

Implemented:

- Telemetry Collection

- Query Analytics

- Log Visibility

---

### Alert Engineering

Configured:

- Metric Alerts

- CPU Threshold

- Email Notifications

---

# 🔥 Incident Simulation

Stress utility:

```bash
sudo apt update

sudo apt install stress -y

stress --cpu 4 --timeout 600
```

Validated:

✅ CPU Spike

✅ Alert Trigger

✅ Email Notification

✅ Dashboard Visibility

---

# 📑 KQL Query Examples

## CPU Query

```kql
InsightsMetrics

| where Namespace=="Processor"

| summarize AvgCPU=avg(Val)

by bin(TimeGenerated,5m)

| render timechart
```

---

## Heartbeat Query

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

![VM Monitoring](images/vm-monitoring-dashboard.PNG)

---

## Network Dashboard

![Network Dashboard](images/network-monitoring-dashboard.PNG)

---

## Disk Monitoring

![Disk Monitoring](images/disk-monitoring-dashboard.PNG)

---

## Azure Monitor

![Azure Monitor](images/azure-monitor-onboarding.PNG)

---

## CPU Alert Rule

![CPU Alert](images/cpu-alert-rule-configuration.PNG)

---

## Email Notification

![Email Notification](images/email-alert-notification.PNG)

---

## Alert Dashboard

![Alert Dashboard](images/alerts-dashboard.PNG)

---

## Heartbeat Query

![Heartbeat](images/heartbeat-kql-query.PNG)

---

## CPU Stress Testing

![CPU Stress](images/linux-cpu-stress-testing.PNG)

---

## Deployment Validation

![Deployment](images/monitoring-deployment-complete.PNG)

---

# ⚠️ Engineering Challenges Solved

| Challenge | Solution |
|---|---|
| SSH Failure | Native SSH + PEM |
| Missing Alerts | CPU Stress Validation |
| Logs Missing | AMA Validation |
| Cost Issue | Bastion Removal |

---

# 🧠 Skills Demonstrated

Azure Monitor

Azure Alerts

KQL

Azure Workbooks

Cloud Monitoring

Incident Engineering

Observability Engineering

Dashboard Visualization

Linux Administration

Operational Visibility

Cloud Operations

SRE Practices

---

# 📈 Business Outcome

Successfully implemented cloud-native monitoring platform supporting:

✅ Incident Detection

✅ Infrastructure Visibility

✅ Alert Engineering

✅ Dashboard Visualization

✅ Linux Monitoring

✅ Operational Troubleshooting

---

# 👨‍💻 Author

## Amit Kumar

Cloud Engineer | Azure Administrator | Observability Engineer

GitHub

https://github.com/Akamitt009

LinkedIn

https://www.linkedin.com/in/amit-kumar-657255232/
