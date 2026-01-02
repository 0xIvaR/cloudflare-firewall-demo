# Cloud-Based Firewall for Website Protection

🔗 **Live Demo:** [sohamkunduivar.me](https://sohamkunduivar.me)

## Project Overview

A cloud-based firewall implementation using **Cloudflare** to protect a live website. This project demonstrates enterprise-grade web security including WAF (Web Application Firewall), DDoS protection, rate limiting, and real-time threat monitoring.

## 🌐 Protected Website

| Property | Value |
|----------|-------|
| **Domain** | `sohamkunduivar.me` |
| **Hosting** | GitHub Pages |
| **CDN/Firewall** | Cloudflare |
| **SSL/TLS** | Full (Strict) |

## 🛡️ Security Features

- **Web Application Firewall (WAF)** - Protection against OWASP Top 10 vulnerabilities
- **DDoS Protection** - Unlimited mitigation against volumetric attacks
- **Rate Limiting** - Prevent brute force and abuse
- **Bot Protection** - Block malicious automated traffic
- **SSL/TLS Encryption** - End-to-end HTTPS security

## 🔧 Technologies Used

| Technology | Purpose |
|------------|---------|
| Cloudflare | Cloud firewall, CDN, DNS |
| GitHub Pages | Static website hosting |
| DNS/Nameservers | Domain routing |
| HTTPS | Secure communication |

## 📊 Architecture

```
┌─────────────┐      ┌──────────────────┐      ┌─────────────────┐
│   Visitor   │─────▶│    Cloudflare    │─────▶│  GitHub Pages   │
│   Browser   │      │    (Firewall)    │      │ (Origin Server) │
└─────────────┘      └──────────────────┘      └─────────────────┘
                              │
                     ┌────────┴────────┐
                     │ Security Layer  │
                     │ • WAF Rules     │
                     │ • Rate Limiting │
                     │ • Bot Detection │
                     │ • DDoS Shield   │
                     └─────────────────┘
```

## 📈 Project Status

| Step | Description | Status |
|------|-------------|--------|
| 1 | Domain & Hosting Setup | ✅ Complete |
| 2 | Cloudflare Integration | ✅ Complete |
| 3 | Firewall Rules (5 Custom + 1 Rate Limit) | ✅ Complete |
| 4 | WAF Configuration | ✅ Complete |
| 5 | Monitoring & Analytics | ✅ Complete |
| 6 | Final Documentation | ✅ Complete |

## 🎯 Deliverables

- ✅ Live protected website
- ✅ 5 Custom firewall rules + 1 Rate limiting rule
- ✅ WAF with OWASP Core Ruleset
- ✅ Security monitoring dashboard
- ✅ OWASP Top 10 protection mapping
- ✅ 100% attack block rate verified

## 🧪 Test Results

| Attack Type | Result |
|-------------|--------|
| SQL Injection | 🛡️ Blocked |
| XSS Attacks | 🛡️ Blocked |
| Path Traversal (.env, .git) | 🛡️ Blocked |
| Malicious Bots (sqlmap) | 🛡️ Blocked |
| Normal Traffic | ✅ Allowed |

---

## Author
Soham Kundu | Internship Project 2026
