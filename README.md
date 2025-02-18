# 🛡️ Securing an Environment with Azure Security Center & Azure Sentinel

## 📄 Overview

This project demonstrates the setup and configuration of **Azure Security Center** and **Azure Sentinel** to secure a cloud environment. It includes enabling security policies, configuring threat detection, and analyzing security incidents.

---

## 🧑‍💻 Key Focus Areas:

- **Azure Security Center** for posture management and security recommendations.
- **Azure Sentinel** for Security Information and Event Management (SIEM) and Security Orchestration, Automation, and Response (SOAR).
- **Threat Detection**: Real-time monitoring, alerts, and incident investigation.

---

## 🛠️ Project Implementation Steps

### 1️⃣ **Azure Security Center Setup**

- Enable **Azure Security Center Standard Tier**.
- Configure **Security Policies**.
- Enable **Azure Defender for Servers, SQL, Storage, and App Services**.
- View **Secure Score** and implement recommendations.



---

### 2️⃣ **Azure Sentinel Deployment**

- Activate **Azure Sentinel** on the Log Analytics workspace.
- Connect Data Sources.
- Configure **Analytic Rules** for automated threat detection.
- Create **Hunting Queries** and **Workbooks** for visualization.



---

### 3️⃣ **Threat Detection and Incident Analysis**

- Set up **Alerts** in **Security Center**.
- Monitor **Incidents** in **Sentinel**.
- Investigate security incidents using **Log Search Queries (KQL)**.
- Automate threat response using **Playbooks**.

---

## ⚙️ Analysis Script – `security_alerts_analysis.py`

```python
import pandas as pd

# Alert data simulation
data = {
    'AlertName': ['Malware Detected', 'Unusual Sign-In', 'SQL Injection Attempt'],
    'Severity': ['High', 'Medium', 'High'],
    'Status': ['New', 'Resolved', 'New'],
    'Description': [
        'Malware detected on VM1',
        'Suspicious sign-in from unknown IP',
        'SQL injection attempt on web app'
    ]
}

alerts_df = pd.DataFrame(data)

# Display high-severity incidents
high_severity_alerts = alerts_df[alerts_df['Severity'] == 'High']

print("High Severity Security Alerts:")
print(high_severity_alerts)
```
