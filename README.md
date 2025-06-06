# Internship-ElevateLabs

##  Task 1: Nmap TCP SYN Scan on Local IP

As part of my internship, I performed a TCP SYN scan on my local IP using **Nmap**.

### Nmap installation:

![nmap_installation](https://github.com/user-attachments/assets/873e7c0b-66ed-4954-825e-ead6f96e16e5)

### Command Used:

sudo nmap -sS 192.168.43.157

### Scan Result:

![nmap_scan_result](https://github.com/user-attachments/assets/4dc1a249-ca1d-4681-a4e7-b79c232c0fcd)

---

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

---

#  Task 3: Perform a Basic Vulnerability Scan on Your PC.

As part of my cybersecurity internship, I conducted a vulnerability scan on my local machine using **OpenVAS** (Greenbone Community Edition).

---

##  Tools & Environment

- **Operating System**: Ubuntu 22.04 LTS
- **Scanner**: OpenVAS (Greenbone Vulnerability Management)
- **Scan Type**: Full and Fast Scan
- **Target**: 192.168.43.157 (Localhost)

---

## Steps Followed

1. Installed OpenVAS using `sudo apt install openvas` and initialized with `gvm-setup`.
2. Configured target (localhost) and created a new task in GVM dashboard.
3. Executed a **Full and Fast Scan**.
4. Waited ~1 hour for the scan to complete.
5. Analyzed the report for vulnerabilities.
6. Documented top critical vulnerabilities and provided mitigation suggestions.
---

#  Task 4: Setup and Use a Firewall on Windows/Linux

As part of my cybersecurity internship, I completed a hands-on task configuring a firewall on Linux using **UFW (Uncomplicated Firewall)**.

---

##  Objective

To understand how firewall rules manage network traffic and to demonstrate rule creation, testing, and deletion.

---

##  Environment

- **OS**: Ubuntu 22.04 LTS  
- **Tool**: UFW (Uncomplicated Firewall)

---

##  Steps Performed

1. **Checked UFW status** to ensure the firewall is active.
2. **Blocked port 23 (Telnet)** to prevent insecure remote access.
3. **Tested the block** using `telnet` (or `nc` to simulate).
4. **Allowed SSH (port 22)** to ensure remote admin access is maintained.
5. **Removed the test block rule** to restore the original configuration.
6. Captured terminal screenshots of commands and results.
---

#  Task 5: Capture and Analyze Network Traffic Using Wireshark.

This task was completed as part of my Cybersecurity Internship to explore packet capturing, protocol filtering, and basic network analysis using Wireshark.

---

##  Tools & Setup

- **OS**: Ubuntu 22.04 LTS  
- **Tool Used**: Wireshark  
- **Network Interface**: wlo1 (Wi-Fi)  

---

##  Steps Performed

1. Installed Wireshark using `sudo apt install wireshark`.
2. Ran Wireshark and selected the active Wi-Fi interface (`wlo1`).
3. Started packet capture.
4. Browsed a few websites and ran `ping google.com` in terminal to generate traffic.
5. Stopped capture after ~1 minute.
6. Applied filters (`dns`, `http`, `icmp`) to analyze packets by protocol.

---

##  Protocols Observed

- **DNS**: Domain resolution queries.
- **HTTP**: Web requests and responses in plaintext.
- **ICMP**: Echo requests and replies from ping command.

---

##  Key Concepts

- Packet and protocol analysis
- Live capture with Wireshark
- Filtering network traffic by protocol
- Role of DNS, HTTP, ICMP in everyday usage

---


#  Task 6: Create a Strong Password and Evaluate Its Strength.

This task involved testing the strength of different passwords and learning how password complexity affects overall security.

---

##  System Info

- **Operating System**: Ubuntu 22.04 LTS  
- **Tool Used**: [passwordmeter.com](https://www.passwordmeter.com)

---

##  Steps Followed

1. Created 5 passwords with varying complexity.
2. Tested each on passwordmeter.com.
3. Recorded strength score and feedback.
4. Noted best practices for creating strong passwords.
5. Researched common password attacks and defense mechanisms.

---

##  Summary of Results

| Password             | Score  | Strength         |
|----------------------|--------|------------------|
| Password123          | 30%    | Weak             |
| K@rTh!k@2024         | 80%    | Strong           |
| tadiPurnaK@rthik#57  | 95%    | Very Strong      |
| 12345678             | 10%    | Extremely Weak   |
| Ubuntu_Rocks@22      | 85%    | Strong           |

---

##  Key Concepts Learned

- Password complexity and entropy
- Brute force and dictionary attacks
- Benefits of passphrases
- Importance of multi-factor authentication (MFA)

---
#  Task 7: Identify and Remove Suspicious Browser Extensions

This task aimed to raise awareness about browser security by auditing installed extensions and identifying potentially risky add-ons.

---

## System Details

- **Operating System**: Ubuntu 22.04 LTS  
- **Browser Used**: Google Chrome  
- **Extension Page Used**: `chrome://extensions/`

---

##  Steps Performed

1. Opened the Chrome Extensions page.
2. Reviewed all installed extensions.
3. Checked each extension's:
   - Permissions
   - Reviews and user ratings
   - Publisher identity
4. Removed unnecessary or suspicious ones.
5. Restarted the browser to check performance.

---

##  Extensions Removed

| Extension Name         | Reason for Removal                                |
|------------------------|----------------------------------------------------|
| Video Downloader Pro   | Unknown publisher, high permissions, poor reviews  |
| Screen Capture Tool    | Rarely used, lacked trust indicators               |

---

## Extensions Kept

| Extension Name     | Reason |
|--------------------|--------|
| Grammarly          | Trusted, widely used, verified developer |
| Dark Reader        | Open-source, useful, minimal permissions |
| Momentum           | Well-rated, productivity extension        |

---

##  Key Takeaways

- Extensions with high permissions and unknown publishers can be dangerous.
- Always check reviews and permissions before installing.
- Remove unused extensions to reduce attack surface.
- Keep browser updated and extensions minimal.

---
# Task 8: Working and Understanding the VPN

This task involved installing and using a VPN on Ubuntu 22.04 to understand how VPNs help protect user privacy, encrypt traffic, and mask online identity.

---

##  Environment

- **OS**: Ubuntu 22.04 LTS  
- **VPN Service**: ProtonVPN (Free Tier)  
- **Tool Used**: ProtonVPN CLI

---

##  Steps Followed

1. Installed ProtonVPN CLI with `sudo apt install protonvpn-cli`.
2. Logged in and connected to a free VPN server.
3. Verified IP change via `whatismyipaddress.com`.
4. Browsed websites to confirm traffic redirection and encryption.
5. Disconnected and compared performance before/after.

---

##  Results

| Test                            | Observation                          |
|----------------------------------|--------------------------------------|
| VPN Connection                   | Successful                           |
| IP Changed                       | Yes (new server location shown)      |
| Traffic Encrypted                | Yes (via HTTPS and VPN tunnel)       |
| Browsing Speed                   | Slightly slower but stable           |
| VPN Protocol Used                | OpenVPN                              |

---

## Key Concepts Learned

- VPN encrypts internet traffic and hides IP addresses.
- VPN helps protect against surveillance and public Wi-Fi attacks.
- Common protocols: OpenVPN, WireGuard, IKEv2.
- VPN ≠ complete anonymity — still need safe practices.

---











