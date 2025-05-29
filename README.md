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




