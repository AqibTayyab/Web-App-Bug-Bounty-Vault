### 📜 **HTTP Protocol Cheat Sheet (For Hackers)**

#### **1. The Methods (Kaam kya ho raha hai?)**

|**Method**|**Normal Kaam**|**Hacker Ki Nazar (Vulnerability)**|
|---|---|---|
|**GET**|Data mangwana (Fetch).|**Info Leak:** Kya sensitive data URL mein aa raha hai? (History logs mein save hoga).|
|**POST**|Data bhejna (Submit).|**Logic Bugs:** Kya main `-1` quantity bhej sakta hon? Kya main ID change kar sakta hon?|
|**PUT**|Data update karna.|**Unauthorized Access:** Kya main kisi aur ki profile update kar sakta hon?|
|**DELETE**|Data delete karna.|**Privilege Escalation:** Kya main admin ka account delete kar sakta hon bina admin hue?|

---

#### **2. Status Codes (Server ka Mood)**

Yeh codes server ki zubaan hain. Rat lo inhe:

|**Code**|**Matlab (Meaning)**|**Hacker Action (Kya karna hai?)**|
|---|---|---|
|**200 OK**|Sab theek hai. ✅|Response body check karo, shayad hidden info mil jaye (comments, API keys).|
|**301/302**|Redirect (Yahan se jao). ➡️|**Open Redirect:** Check karo ke `?next=google.com` laga kar kisi aur site par bhej sakte ho?|
|**401**|Unauthorized (Login karo). 🔒|Default credentials try karo (`admin:admin`, `root:toor`).|
|**403**|Forbidden (Andar aana mana hai). 🚫|**Bypass Try Karo:** Headers change karo (`X-Forwarded-For: 127.0.0.1`) ya IDOR try karo.|
|**404**|Not Found (Kuch nahi mila). ❌|**Fuzzing:** Shayad file ka naam alag ho? (`/backup`, `/admin.bak`, `/secret`).|
|**500**|Server Error (Dhamaka). 💥|**Jackpot:** Server confuse ho gaya. **SQL Injection** (`' OR 1=1`) ya input validation bugs dhoondo.|

---

### 3. Critical Headers (Injection Points)

Request ke "Metadata" ko change kar ke server ko fool banao.

- **User-Agent:** Browser ki pehchan.
    
    - _Hack:_ Isay `Googlebot` ya `iPhone` kar ke dekho. Shayad hidden content mil jaye.
        
    - _Attack:_ SQLi payload yahan bhi chalta hai!
        
- **Referer:** Tum kahan se aaye ho.
    
    - _Hack:_ Security checks aksar yahan fail hotay hain.
        
- **X-Forwarded-For:** Asli IP.
    
    - _Hack:_ `127.0.0.1` likh kar IP bans bypass karo.
        
- **Host:** Kis domain par jana hai.
    
    - _Hack:_ **Host Header Injection** (Password reset links hijack karne ke liye).
        

---

### 4. Cookies & Sessions (Identity)

Sabse qeemti cheez.

|**Component**|**Description**|**Security Risk**|
|---|---|---|
|**Session ID**|Server ka diya hua Token.|**Session Hijacking:** Agar ye chori hua, toh Account Hack.|
|**HttpOnly**|JavaScript access rokta hai.|**False = Critical.** XSS ke zariye cookie chori ho sakti hai.|
|**Secure**|Sirf HTTPS par chalega.|**False = Weak.** Man-in-the-Middle attack se cookie chori ho sakti hai.|
|**SameSite**|Cross-site request policy.|**None/Lax = CSRF Risk.** Doosri site se request bheji ja sakti hai.|

---

### 5. Networking Basics (Finding the Target)

**DNS (Phonebook):**

- **Record A:** Domain -> IPv4 (`192.168.1.1`).
    
- **CNAME:** Alias (`shop.com` -> `shopify.com`). _Subdomain Takeover yahan milta hai._
    
- **NS (Name Server):** DNS kaun sambhaal raha hai? (Cloudflare, AWS, etc.).
    

**Ports (Darwazay):**

Agar `Nmap` scan karo toh ye numbers yaad rakho:

|**Port**|**Service**|**Attack Vector**|
|---|---|---|
|**21**|FTP (File Transfer)|Anonymous Login try karo.|
|**22**|SSH (Remote Access)|Brute Force (Weak passwords).|
|**25**|SMTP (Email)|Email Spoofing / User Enumeration.|
|**80/443**|HTTP/HTTPS (Web)|Web Attacks (XSS, SQLi, IDOR).|
|**3306**|MySQL (Database)|Direct Database Access (agar open hai).|
|**8080**|Alt Web|Developers ka testing server (Aksar less secure).|

---

### 6. Essential Commands (Toolbelt)

Apne terminal (Kali Linux) par ye commands yaad rakho:

- **IP Check:** `ping target.com` (IP aur server status dekhne ke liye).
    
- **DNS Info:** `nslookup target.com` (Records check karne ke liye).
    
- **Port Scan (Fast):** `nmap -F target.com` (Top 100 ports scan).
    
- **Port Scan (Service Info):** `nmap -sC -sV target.com` (Version aur OS detection).
    
- **Burp Suite:** `Ctrl + R` (Request ko Repeater mein bhejne ke liye).

---
