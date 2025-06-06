# Internship-ElevateLabs

##  Task 1: Nmap TCP SYN Scan on Local IP

As part of my internship, I performed a TCP SYN scan on my local IP using **Nmap**.

### Nmap installation:

![nmap_installation](https://github.com/user-attachments/assets/873e7c0b-66ed-4954-825e-ead6f96e16e5)

### Command Used:

sudo nmap -sS 192.168.43.157

### Scan Result:

![nmap_scan_result](https://github.com/user-attachments/assets/4dc1a249-ca1d-4681-a4e7-b79c232c0fcd)

## Task 2: Phishing Email Analysis

### Sample Email :-
![phising](https://github.com/user-attachments/assets/4f26d730-8db8-44bf-9e88-6dfa065a10d3)

Subject: **Microsoft account password change**  
Sender: `support@msupdate.net`  
Recipient: `ethan@hooksecurity.co`  

---

### Observations

1. **Sender Email Spoofing**  
   - The email claims to be from Microsoft, but the sender address is `support@msupdate.net`, which is **not a valid Microsoft domain**.

2. **Suspicious Links**  
   - The message contains links to reset the password, review security info, and learn more. Since the domain is not verified as Microsoft's, these links are **likely redirecting to phishing pages** (hover-over would confirm mismatches).

3. **Social Engineering (Urgency)**  
   - The email creates urgency by claiming, “If this wasn't you, your account has been compromised,” pressuring the user to act quickly.

4. **No Personalization**  
   - The email does not include the user's name or specific details—common in bulk phishing emails.

5. **Generic Signature**  
   - Signed by “The Microsoft account team” without official branding or contact details.

6. **Impersonation of Legitimate Format**  
   - The design mimics a real Microsoft alert email but lacks Microsoft’s secure footer or digital signature.

---

### Tools Used
- Manual inspection (visual and sender analysis)
- Link hover (recommended for future live analysis)
- Email header analyzers (e.g., MXToolbox, if full headers available)

---

### Conclusion
This email is **highly suspicious and likely a phishing attempt**. It spoofs Microsoft's identity, uses social engineering, and contains unverified links. The user should not click any links and report this email as phishing.

# 🔍 Task 3: Perform a Basic Vulnerability Scan on Your PC.

As part of my cybersecurity internship, I conducted a vulnerability scan on my local machine using **OpenVAS** (Greenbone Community Edition).

---

## 🧰 Tools & Environment

- **Operating System**: Ubuntu 22.04 LTS
- **Scanner**: OpenVAS (Greenbone Vulnerability Management)
- **Scan Type**: Full and Fast Scan
- **Target**: 192.168.43.157 (Localhost)

---

## ⚙️ Steps Followed

1. Installed OpenVAS using `sudo apt install openvas` and initialized with `gvm-setup`.
2. Configured target (localhost) and created a new task in GVM dashboard.
3. Executed a **Full and Fast Scan**.
4. Waited ~1 hour for the scan to complete.
5. Analyzed the report for vulnerabilities.
6. Documented top critical vulnerabilities and provided mitigation suggestions.

# 🔥 Task 4: Setup and Use a Firewall on Windows/Linux

As part of my cybersecurity internship, I completed a hands-on task configuring a firewall on Linux using **UFW (Uncomplicated Firewall)**.

---

## 🎯 Objective

To understand how firewall rules manage network traffic and to demonstrate rule creation, testing, and deletion.

---

## 💻 Environment

- **OS**: Ubuntu 22.04 LTS  
- **Tool**: UFW (Uncomplicated Firewall)

---

## 🧪 Steps Performed

1. **Checked UFW status** to ensure the firewall is active.
2. **Blocked port 23 (Telnet)** to prevent insecure remote access.
3. **Tested the block** using `telnet` (or `nc` to simulate).
4. **Allowed SSH (port 22)** to ensure remote admin access is maintained.
5. **Removed the test block rule** to restore the original configuration.
6. Captured terminal screenshots of commands and results.







