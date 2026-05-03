# 🎬 CineBook Pro – Secure Web Application Deployment

## 🚀 Project Overview

CineBook Pro is a simple web-based movie booking application developed and deployed as part of the **SecureStack Mission**. The project demonstrates not only application deployment but also the implementation of essential cybersecurity practices.

The application is hosted on Microsoft Azure and is publicly accessible over the internet.

---

## 🌐 Live Application

🔗 https://cinebook-app.azurestaticapps.net

---

## ☁️ Deployment Details

* **Platform:** Microsoft Azure (Static Web Apps)
* **Source Code:** GitHub Repository
* **Deployment Method:** Continuous Deployment via GitHub Actions
* **Hosting Type:** Static Web Hosting

---

## ⚙️ Deployment Steps

1. Created a GitHub repository and uploaded project files
2. Connected GitHub repository to Azure Static Web Apps
3. Configured build settings:

   * App location: `/`
   * Output location: `.`
4. Deployed application using Azure portal
5. Verified successful deployment using public URL

---

## 🛡️ Firewall Implementation

A firewall was implemented using Azure Network Security Group (NSG) to control inbound traffic.

### 🔹 Configured Rules

| Priority | Rule Name   | Port | Protocol | Action |
| -------- | ----------- | ---- | -------- | ------ |
| 100      | Allow-HTTP  | 80   | TCP      | Allow  |
| 110      | Allow-HTTPS | 443  | TCP      | Allow  |
| 65500    | Deny-All    | Any  | Any      | Deny   |

### 🔹 Description

* Only HTTP and HTTPS traffic is allowed
* All other inbound traffic is blocked
* Default Azure deny rule ensures complete restriction

---

## 🔐 Security Compliance (OWASP Top 10)

| OWASP ID | Vulnerability                  | Mitigation                                                                |
| -------- | ------------------------------ | ------------------------------------------------------------------------- |
| A1       | Broken Access Control          | Session-based authentication                                              |
| A2       | Cryptographic Failures         | SHA-256 hashing with salt for password security                           |
| A3       | Cross-Site Scripting (XSS)     | Input sanitization using `escapeHtml()` and Content Security Policy (CSP) |
| A5       | Security Misconfiguration      | Security headers (CSP, X-Frame-Options)                                   |
| A7       | Identification & Auth Failures | Strong password policy (minimum 6 characters)                             |

---

## 🔒 Additional Security Measures

* 🔐 **HTTPS Enforcement** – Secure communication using SSL/TLS
* 🧱 **Content Security Policy (CSP)** – Prevents script injection
* 🚫 **X-Frame-Options** – Protects against clickjacking
* 🧼 **Input Validation & Sanitization** – Prevents XSS attacks
* 🔑 **Authentication System** – Session-based login implemented
* 🔄 **Automatic Updates** – Managed by Azure platform

---

## 🌐 Network Security

* Only essential ports are exposed:

  * **Port 80 (HTTP)** – Redirected to HTTPS
  * **Port 443 (HTTPS)** – Secure traffic
* All other ports are blocked by firewall configuration
* Azure provides built-in DDoS protection

---

## 🎯 Security Justification

The system implements multiple layers of security including firewall restrictions, input validation, secure authentication, and encrypted communication. By allowing only essential ports (80 and 443), the attack surface is minimized. Azure’s managed infrastructure further enhances security with built-in protections.

---

## 📌 Conclusion

The CineBook Pro application was successfully deployed on Microsoft Azure with proper security configurations. The implementation of firewall rules, secure coding practices, and cloud-based protections ensures a safe and reliable web application.

---

## 👨‍💻 Author

**Abhishek P Suresh**

---
