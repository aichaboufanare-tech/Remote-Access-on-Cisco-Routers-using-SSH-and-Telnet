# Remote-Access-on-Cisco-Routers-using-SSH-and-Telnet
# Remote Access on Cisco Routers – SSH &amp; Telnet  This project demonstrates how to configure **remote access** on a **Cisco CSR1000v router** using **SSH and Telnet**, with secure and professional settings.  ---
---

## 1️⃣ Basic Setup

- Router Name: `R1`
- Management IP: `192.168.1.1/24`
- Management Interface: `GigabitEthernet1`

### Configuration Steps

1. Set router hostname and domain name (required for SSH)
2. Create a local user with full privileges
3. Generate RSA SSH keys
4. Enable SSH v2 and set security options
5. Configure VTY lines for Telnet and SSH
6. Save configuration

---

## 2️⃣ Testing Remote Access from a PC

### Telnet
```bash
telnet 192.168.1.1

SSH

ssh admin@192.168.1.1

    ⚠️ Note: Older systems like Windows XP may not support SSH due to lack of modern encryption. Use Windows 10, Linux, or PuTTY instead.

3️⃣ Common Issues

    Some router models or old IOS versions do not support SSH v2.

    Windows XP may fail to connect via SSH.

    Telnet may not work due to VTY configuration or security restrictions.

4️⃣ SSH vs Telnet
Feature	SSH	Telnet
Encryption	Fully encrypted	Not encrypted
Security	High	Low
Protocol	TCP 22	TCP 23
Usage	Secure remote administration	Labs or testing only
Recommended	✅ SSH	❌ Telnet

    Pro Tip: Always use SSH instead of Telnet in production networks to protect credentials and data.

5️⃣ Summary

    SSH: Secure, recommended for all production networks.

    Telnet: Unencrypted, only for testing or legacy environments.

    Local User: Always create strong credentials.

    GNS3 / CSR1000v: Fully compatible with this configuration.``
