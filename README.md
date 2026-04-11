# 💀 VulnHub Writeups

Structured writeups of VulnHub boot2root machines — documented with full enumeration, exploitation, and privilege escalation steps.

![Status](https://img.shields.io/badge/Status-Active-brightgreen) ![Machines](https://img.shields.io/badge/Machines_Rooted-4-blue) ![Platform](https://img.shields.io/badge/Platform-VulnHub-orange) ![Focus](https://img.shields.io/badge/Focus-Offensive_Security-darkred)

*Full process documented — recon to root, including what failed and why.*

---

## 🖥️ Machines

| Machine | OS | Difficulty | Author | Key Techniques |
|---------|-----|------------|--------|----------------|
| [DC-1](./DC-1) | Linux (Debian) | Easy | DCAU | Drupal CMS, Drupalgeddon2, SUID exploitation |
| [DC-2](./DC-2) | Linux (Debian) | Easy | DCAU | WordPress, WPScan, CeWL, rbash escape, sudo git |
| [MR-ROBOT](./MR-ROBOT) | Linux (CentOS) | Medium | Leon Johnson | WordPress, WPScan, reverse shell, SUID nmap, privilege escalation |
| [STAPLER](./STAPLER) | Linux | Medium | g0tm1lk. | Multi-service enum, multiple entry points, complex wordpress attack |

---

## ⚙️ Methodology

Every machine follows the same structured approach:

    Reconnaissance     →  passive info gathering
           ↓
    Enumeration        →  nmap, gobuster, wpscan, nikto
           ↓
    Vulnerability      →  manual analysis, CVE lookup
    Discovery
           ↓
    Exploitation       →  metasploit / manual
           ↓
    Privilege          →  linpeas, SUID, sudo -l, GTFOBins
    Escalation
           ↓
    Post Exploitation  →  flags, loot

---

## 🔍 Machine Summaries

### DC-1

A purposely built vulnerable lab designed as a beginner-friendly boot2root challenge. Runs **Drupal 7** on Apache, exploitable via Drupalgeddon2. Privilege escalation achieved through a misconfigured SUID permission on `/usr/bin/find`. Contains 5 flags with the ultimate goal of reading the flag in root's home directory.

- **Ports:** 22 (SSH), 80 (HTTP - Drupal 7), 111 (RPCBind)
- **Exploit:** Drupalgeddon2 (CVE-2018-7600)
- **PrivEsc:** SUID on `/usr/bin/find` via GTFOBins

---

### DC-2

A follow-up to DC-1, also beginner-friendly. Runs **WordPress** on Apache. Requires generating a custom wordlist with CeWL, brute forcing credentials with WPScan, SSH login as Tom, escaping a restricted bash shell via Vi, switching to Jerry, then exploiting sudo git for root.

- **Ports:** 80 (HTTP - WordPress), 7744 (SSH)
- **Exploit:** WPScan brute force with CeWL wordlist
- **PrivEsc:** rbash escape via Vi, sudo git via GTFOBins

---

### MR-ROBOT

Based on the Mr. Robot TV show, this medium-difficulty machine runs **WordPress** on Apache. Requires enumerating hidden paths via robots.txt, generating a wordlist from the site with CeWL, brute forcing WordPress credentials with WPScan, uploading a reverse shell via the theme editor, then escalating privileges using a SUID bit set on nmap.

- **Ports:** 80 (HTTP - WordPress), 443 (HTTPS), 22 (SSH - filtered)
- **Exploit:** WordPress reverse shell via theme editor
- **PrivEsc:** SUID nmap interactive mode via GTFOBins

---

### STAPLER-1

Created for BSidesLondon 2016, this beginner-to-intermediate machine is a "kitchen sink" of vulnerabilities with multiple entry points and potential rabbit holes. It requires heavy enumeration across several services, identifying sensitive files via anonymous FTP and SMB, and performing a WordPress attack using an LFI vulnerability or plugin exploitation to gain an initial shell.

- **Ports:** 21 (FTP), 22 (SSH), 53 (DNS), 80/12380 (HTTP/HTTPS - WordPress), 139/445 (SMB), 3306 (MySQL)
- **Exploit:** WordPress LFI to read wp-config.php or a malicious plugin upload for a reverse shell.
- **PrivEsc:** Local kernel exploit (e.g., Ubuntu 16.04 "double-put") or exploiting world-writable cron jobs/scripts.
  
---

## 🛠️ Tools Used

![Nmap](https://img.shields.io/badge/-Nmap-blue) ![Metasploit](https://img.shields.io/badge/-Metasploit-blueviolet) ![WPScan](https://img.shields.io/badge/-WPScan-red) ![CeWL](https://img.shields.io/badge/-CeWL-orange) ![GTFOBins](https://img.shields.io/badge/-GTFOBins-black) ![Nikto](https://img.shields.io/badge/-Nikto-green) ![ffuf](https://img.shields.io/badge/-ffuf-yellow)

---

## 📁 Each Machine Folder Contains

- Full notes with commands and actual output
- Reasoning behind every step taken
- Screenshots of key findings
- Dead ends — what didn't work and why

---

## ⚠️ Disclaimer

All machines documented here are **intentionally vulnerable systems** hosted on VulnHub.
These techniques are practiced strictly for educational purposes.
Never test systems without explicit authorization.

---

*Adarsh Dubey · Cybersecurity Student*
