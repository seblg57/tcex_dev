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
```bash
tcex package
tcex install

## 🖼️ Example Playbook Execution

![Netcheck Playbook](./screenshot_playbook.png)
