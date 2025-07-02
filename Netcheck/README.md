# 🔍 Netcheck - ThreatConnect Playbook App

Netcheck is a custom Playbook App for **ThreatConnect** that performs a complete network diagnostic for a given hostname and port.

It checks:
- ✅ DNS resolution
- 🔐 SSL certificate validity and cipher suite
- 🌐 HTTPS connectivity

This utility is ideal for verifying threat intelligence sources, validating domain configurations, or conducting security assessments within your ThreatConnect workflows.

## 🚀 Features
- Fast IP resolution and DNS check
- TLS handshake and certificate CN extraction
- SSL cipher suite detection
- HTTPS GET request test (port configurable, default 443)

## 🛠️ Requirements
- ThreatConnect version **7.2.0+**
- Python 3.11
- TCEx SDK `>=4.0.0,<4.1.0`

## 📦 Installation
Import the app via **TC Exchange** or deploy it manually with:


## 🖼️ Example Playbook Execution


![Screenshot_1190](https://github.com/user-attachments/assets/2f1ca32c-aa91-446c-9f79-8db415eef276)
![Screenshot_1191](https://github.com/user-attachments/assets/e1a26ea4-dc8e-4989-a876-db39740abc49)
