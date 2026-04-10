# Incident Report — WarmCookie Infection
 
**Date:** 2024-08-15
**Malware Family:** WarmCookie

---
 
## Executive Summary

On August 15, 2024, the machine DESKTOP-H8ALZBV belonging to Pierce Lucero was compromised with WarmCookie malware.
 
---
 
## Victim Details
 
| Field | Value |
|---|---|
| **Hostname** | `DESKTOP-H8ALZBV` |
| **IP Address** | `10.8.15.133` |
| **MAC Address** | `00:1c:bf:03:54:82` |
| **Windows Username** | `plucero` |
| **AD Domain** | `lafontainebleu.org` |
 
---
 
## Indicators of Compromise
 
### Infection Chain
 
1. ZIP lure downloaded from `quote.checkfedexexp.com` (HTTP)
2. Unknown follow-up download from `business.checkfedexexp.com` (HTTPS)
3. DLL payload downloaded via BITS over HTTP from `72.5.43.29`
4. Post-infection GET and POST activity observed
 
### Domains
 
| Domain | Role |
|---|---|
| `quote.checkfedexexp.com` | ZIP lure delivery (HTTP) |
| `business.checkfedexexp.com` | Unknown follow-up download (HTTPS) |
 
### IP Addresses
 
| IP | Notes |
|---|---|
| `104.21.55.70` | Cloudflare — `quote.checkfedexexp.com` |
| `172.67.170.159` | Cloudflare — `business.checkfedexexp.com` |
| `72.5.43.29` | DLL payload server (HTTP/BITS) |
 
### URLs
 
| URL | Description |
|---|---|
| `http://quote.checkfedexexp.com/managements?16553a25e45250a41fd5&...` | ZIP lure download |
| `https://business.checkfedexexp.com/data-privacy?zj=ZzqRKxVRQ&pOd=GEokiOXFwH&sourcedp=tQMQJlIo&Tfocontent=IxGTZjXqxJ&Jr_cid=9464552&L=8174388` | Unkown content download |
| `http://72.5.43.29/data/0f60a3e7baecf2748b1c8183ed37d1e4` | DLL payload via BITS |
 
### Malware Samples
 
| Filename | Type | SHA256 | Size |
|---|---|---|---|
| `Invoice 876597035_003.zip` | ZIP lure | `[ 798563fcf7600f7ef1a35996291a9dfb5f9902733404dd499e2e736ea1dc6fc5 ]` | `[ 2,7MB ]` |
| `[ Invoice-876597035-003-8331775-8334138.js ]` | JS loader | `[ dab98819d1d7677a60f5d06be210d45b74ae5fd8cf0c24ec1b3766e25ce6dc2c ]` | `[ 6,7MB ]` |
| `[ rundll32 ]` | DLL | `[ b7aec5f73d2a6bbd8cd920edb4760e2edadc98c3a45bf4fa994d47ca9cbd02f6 ]` | `[ 156KB ]` |

- Run method: rundll32 [filename],Start
