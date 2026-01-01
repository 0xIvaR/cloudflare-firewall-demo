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
| 2 | Cloudflare Integration | ⏳ Pending |
| 3 | Firewall Rules | ⏳ Pending |
| 4 | WAF Configuration | ⏳ Pending |
| 5 | Monitoring & Analytics | ⏳ Pending |

## 🎯 Deliverables

- ✅ Live protected website
- ⏳ Firewall configuration
- ⏳ WAF rules implementation  
- ⏳ Security monitoring dashboard
- ⏳ OWASP Top 10 protection mapping

---

## Author
Soham Kundu | Internship Project 2026
Internship Project - 2026
