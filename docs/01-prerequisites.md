# Step 1: Prerequisites Setup

## Overview
Before configuring Cloudflare's firewall, we need to establish the foundational components: a live website, a Cloudflare account, and understanding of DNS concepts.

---

## 1.1 Test Website Setup

### Option A: GitHub Pages (Recommended - Free)

1. **Create a GitHub Repository**
   - Go to [github.com](https://github.com) and sign in
   - Click "New Repository"
   - Name it: `firewall-demo-site`
   - Set to **Public**
   - Check "Add a README file"

2. **Upload Website Files**
   - Upload the `website/index.html` file to the repository
   - Go to **Settings → Pages**
   - Under "Source", select `main` branch
   - Click Save
   - Your site will be live at: `https://yourusername.github.io/firewall-demo-site`

3. **Custom Domain (Required for Cloudflare)**
   - You need a custom domain (e.g., from Namecheap, GoDaddy, Freenom)
   - In GitHub Pages settings, add your custom domain
   - This creates a `CNAME` file in your repository

### Option B: Netlify (Alternative - Free)

1. Go to [netlify.com](https://netlify.com)
2. Sign up and click "Add new site"
3. Drag and drop your `website` folder
4. Add custom domain in Site Settings → Domain Management

### Option C: Free Domain Options

| Provider | Free Domain | Notes |
|----------|-------------|-------|
| Freenom | .tk, .ml, .ga, .cf, .gq | May have availability issues |
| GitHub Student | .me domain | Requires student email |
| Namecheap | .me (first year) | With GitHub Student Pack |

---

## 1.2 Cloudflare Account Registration

### Steps to Register:

1. **Go to Cloudflare**
   - Visit [cloudflare.com](https://www.cloudflare.com)
   - Click "Sign Up"

2. **Create Account**
   - Enter your email address
   - Create a strong password
   - Complete email verification

3. **Select Free Plan**
   - Cloudflare offers a generous free tier
   - Includes: Basic WAF, DDoS protection, SSL, CDN

### Free Plan Features:
| Feature | Included |
|---------|----------|
| DDoS Protection | ✅ Unlimited |
| SSL Certificate | ✅ Universal SSL |
| CDN | ✅ Global network |
| Firewall Rules | ✅ 5 custom rules |
| Rate Limiting | ✅ Basic (1 rule) |
| Bot Fight Mode | ✅ Included |
| WAF Managed Rules | ⚠️ Limited (Pro for full) |
| Security Analytics | ✅ Basic dashboard |

---

## 1.3 DNS Concepts Reference

### What is DNS?
DNS (Domain Name System) translates human-readable domain names (e.g., `example.com`) to IP addresses (e.g., `192.168.1.1`).

### Key DNS Record Types:

| Record Type | Purpose | Example |
|-------------|---------|---------|
| **A** | Maps domain to IPv4 address | `example.com → 192.0.2.1` |
| **AAAA** | Maps domain to IPv6 address | `example.com → 2001:db8::1` |
| **CNAME** | Alias to another domain | `www.example.com → example.com` |
| **MX** | Mail server records | `mail.example.com` |
| **TXT** | Text records (verification, SPF) | `v=spf1 include:...` |
| **NS** | Nameserver records | `ns1.cloudflare.com` |

### How Cloudflare Works:

```
┌──────────────┐     ┌─────────────────┐     ┌──────────────────┐
│              │     │                 │     │                  │
│    User      │────▶│   Cloudflare    │────▶│  Origin Server   │
│   Browser    │     │   (Firewall)    │     │  (Your Website)  │
│              │◀────│                 │◀────│                  │
└──────────────┘     └─────────────────┘     └──────────────────┘
                            │
                            ▼
                     ┌─────────────────┐
                     │ Security Checks │
                     │ • WAF Rules     │
                     │ • Rate Limiting │
                     │ • Bot Detection │
                     │ • DDoS Shield   │
                     └─────────────────┘
```

### Nameserver Change Process:

When you add a domain to Cloudflare:
1. Cloudflare scans your existing DNS records
2. You update nameservers at your domain registrar
3. All DNS queries now go through Cloudflare
4. Cloudflare proxies traffic and applies security rules

---

## 1.4 Checklist

Before proceeding to Step 2, ensure you have:

- [ ] A live website accessible via URL
- [ ] A custom domain name (required for Cloudflare)
- [ ] A Cloudflare account (free tier)
- [ ] Access to your domain registrar (to change nameservers)
- [ ] Current DNS records documented

### Document Your Current Setup:

| Item | Your Value |
|------|------------|
| Domain Name | _________________ |
| Current Hosting | _________________ |
| Domain Registrar | _________________ |
| Current Nameservers | _________________ |
| Website IP Address | _________________ |

---

## Next Steps

Once prerequisites are complete, proceed to:
**[Step 2: Integrate Website with Cloudflare](02-cloudflare-integration.md)**

---

## Commands to Verify DNS (Run in Terminal)

```powershell
# Check current DNS records
nslookup yourdomain.com

# Check nameservers
nslookup -type=NS yourdomain.com

# Check A record (IP address)
nslookup -type=A yourdomain.com

# Alternative using PowerShell
Resolve-DnsName yourdomain.com -Type A
Resolve-DnsName yourdomain.com -Type NS
```
