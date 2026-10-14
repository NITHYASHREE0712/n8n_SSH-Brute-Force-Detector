# 🛡️ n8n—SSH Brute-Force Detector

An AI-assisted cybersecurity automation workflow built using n8n, Google Gemini AI, and Telegram.

## 📌 Project Overview

This project detects potentially suspicious SSH login activity by analysing failed login attempts from multiple IP addresses. It assigns a security level and sends alerts to Telegram.

## 🎯 Objectives

- Generate and analyse sample SSH authentication logs.
- Count failed login attempts for each IP address.
- Identify potentially suspicious login activity.
- Mask IP addresses before sending relevant data to the AI Agent.
- Classify activity using AI-assisted analysis.
- Send severity-based alerts through Telegram.

## ⚙️ Technologies Used

- n8n — Workflow automation
- JavaScript — Log processing and severity assignment
- Google Gemini AI — Activity classification
- Telegram Bot — Security notifications

## 🔄 Workflow

1. Manual Trigger starts the workflow.
2. JavaScript generates sample authentication logs and counts failed attempts by IP.
3. The workflow masks the last octet of each IP address before AI analysis.
4. The AI Agent analyses the activity and provides a classification and recommendation.
5. A Switch node routes events according to severity.
6. Telegram sends the corresponding security alert.

## 🚦 Security Levels

| Level | Failed Attempts | Action |
|---|---:|---|
| 🟢 GREEN | 0–2 | Continue monitoring |
| 🟠 ORANGE | 3–5 | Monitor and investigate |
| 🔴 RED | 6 or more | Recommend blocking after human review |

These thresholds are configured for this project demonstration.

## 🔐 Privacy and Safety

The IP address is masked before the relevant data is passed to the AI Agent. The workflow provides recommendations only; it does not automatically block IP addresses.

## 🧪 Testing

The workflow uses synthetic SSH authentication logs for demonstration and testing. It is not connected to a live SSH server.

## 📸 Screenshots

Add screenshots of the n8n workflow execution and the RED, ORANGE, and GREEN Telegram alerts here.

## 🚀 How to Use

1. Download the workflow JSON file from this repository.
2. Open n8n and import the workflow.
3. Configure your own Gemini and Telegram credentials.
4. Execute the workflow and inspect the generated alerts.

## ⚠️ Disclaimer

This project is an educational cybersecurity prototype. It is intended for learning and demonstration purposes.
