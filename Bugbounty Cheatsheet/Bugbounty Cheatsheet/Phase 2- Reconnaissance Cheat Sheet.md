# 🕵️‍♂️ Phase 2: Reconnaissance Cheat Sheet

**Goal:** Target ke baare mein itni info nikalna jitni company ke CEO ko bhi na pata ho.

### 1. Google Dorking (The Search Hack) 🔍

Google se chuphi hui files nikalna.

|**Operator**|**Kaam (Usage)**|**Hacker's Query (Example)**|
|---|---|---|
|`site:`|Sirf is domain mein dhoondo.|`site:tesla.com`|
|`filetype:`|Specific file extension.|`site:gov.pk filetype:pdf "confidential"`|
|`intitle:`|Page ke title mein ye lafz ho.|`intitle:"index of" "backup"` (Directory Listing leak).|
|`inurl:`|URL ke andar ye lafz ho.|`site:target.com inurl:admin` (Admin panel dhoondna).|
|`ext:`|Extension (Log files ke liye).|`site:target.com ext:log|
|`cache:`|Google ka saved version dekho.|`cache:deleted-page.com`|

---

### 2. Tech Stack Identification (Bana Kis Cheez Se Hai?) 🏗️

Vulnerability dhoondne se pehle Technology pata honi chahiye.

|**Tool**|**Kaise Use Karein?**|**Kyun Chahiye?**|
|---|---|---|
|**Wappalyzer**|Browser Extension.|Batata hai: CMS (WordPress?), Server (Nginx?), OS (Linux?).|
|**BuiltWith**|Website (`builtwith.com`).|Detailed profile (Plugins, Analytics, Hosting).|
|**Curl Command**|Terminal: `curl -I target.com`|**Headers Check:** Server version (`Apache 2.4`) leak ho sakta hai.|
|**WhatWeb**|Kali Tool: `whatweb target.com`|Command line se technology scan karta hai.|

---

### 3. Subdomain Hunting (Finding the Weakest Link) 🔗

Main website (`target.com`) secure hoti hai. Subdomains (`dev.target.com`) kamzor hote hain.

|**Type**|**Tool/Website**|**Kaam**|
|---|---|---|
|**Certificate Search**|[`crt.sh`](https://www.google.com/search?q=%5Bhttps://crt.sh/%5D\(https://crt.sh/\))|Query: `%.target.com`. Har wo subdomain jo kabhi register hua.|
|**Search Engines**|Google|`site:target.com -www` (WWW ke ilawa sab dikhao).|
|**Automated Tool**|**Sublist3r** (Kali Linux)|`sublist3r -d target.com` (Auto list nikalta hai).|
|**Brute Force**|**FFuF** / **Gobuster**|Agar subdomain list mein nahi, toh guess karo (`dev`, `test`, `staging`).|

---

### 4. History & Ownership (Maazi aur Maalik) 📜

|**Tool**|**Kaam**|**Hacker's Use Case**|
|---|---|---|
|**Wayback Machine**|`archive.org`|Deleted pages dhoondo (`/admin`, old endpoints).|
|**Whois**|Terminal: `whois target.com`|**Email/Phone:** Phishing ke liye use ho sakta hai. **NameServers:** Cloudflare hai ya nahi?|
|**DNS Dumpster**|Website (`dnsdumpster.com`)|Target ka pura **Map** bana deta hai (Visual graph).|

---

### 5. Recon Workflow (Step-by-Step) ✅

Jab bhi naya target mile, is order mein chalo:

1. **Scope Check:** Kya allowed hai? (`*.target.com` allowed hai ya sirf `www`?).
    
2. **Passive Recon:**
    
    - `whois` (Owner kaun hai?).
        
    - `nslookup` (IP kya hai?).
        
    - `Wappalyzer` (Tech kya hai?).
        
3. **Subdomain Enum:** `crt.sh` aur `Sublist3r` se list banao.
    
4. **Active Scanning:**
    
    - Live subdomains check karo (`httpx`).
        
    - Port Scan (`nmap`).
        
    - Directory Brute Force (`dirb` / `gobuster`).