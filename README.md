# 💀 VulnHub Writeups

Structured writeups of VulnHub boot2root machines — documented with full enumeration, exploitation, and privilege escalation steps.

![Status](https://img.shields.io/badge/Status-Active-brightgreen) ![Machines](https://img.shields.io/badge/Machines_Rooted-7-blue) ![Platform](https://img.shields.io/badge/Platform-VulnHub-orange) ![Focus](https://img.shields.io/badge/Focus-Offensive_Security-darkred)

*Full process documented — recon to root, including what failed and why.*

---

## 🖥️ Machines

| Machine | OS | Difficulty | Author | Key Techniques |
|---------|-----|------------|--------|----------------|
| [DC-1](./DC-1) | Linux (Debian) | Easy | DCAU | Drupal CMS, Drupalgeddon2, SUID exploitation |
| [DC-2](./DC-2) | Linux (Debian) | Easy | DCAU | WordPress, WPScan, CeWL, rbash escape, sudo git |
| [MR-ROBOT](./MR-ROBOT) | Linux (CentOS) | Medium | Leon Johnson | WordPress, WPScan, reverse shell, SUID nmap, privilege escalation |
| [STAPLER](./STAPLER) | Linux | Medium | g0tm1lk. | Multi-service enum, multiple entry points, complex wordpress attack |
| [pWn0S2](./pWn0S2) | Linux | Medium | pWn0S | PHP web exploitation, deeper web attacks |
| [SUNSETDECOY](./SUNSETDECOY) | Linux | Medium | whitecr0wz | Log poisoning, realistic privesc chain, pspy |
| [BRAINPAN-1](./BRAINPAN-1) | Linux (Wine) | Medium | superkojiman | Stack Buffer Overflow, custom exploit dev, sudo GTFOBins |

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

### pWn0S2

A beginner-to-intermediate web-focused machine running Ubuntu 11.04, designed with multiple entry points through its web application. The primary attack path involves enumerating a Simple PHP Blog installation, exploiting an unauthenticated file upload vulnerability to gain remote code execution, and landing a Meterpreter shell as www-data. The machine emphasizes web application enumeration, CVE research, and privilege escalation on an outdated Linux kernel.

- **Ports:** 22 (SSH), 80 (HTTP - Apache 2.2.17, PHP 5.3.5, Simple PHP Blog)
- **Exploit:**  Simple PHP Blog unauthenticated file upload (unix/webapp/sphpblog_file_upload) via Metasploit, achieving RCE as www-data.
- **PrivEsc:** Dirty COW (CVE-2016-5195) kernel exploit targeting Linux 2.6.38, overwriting /etc/passwd to create a root-level user (firefart) OR directory enumeration
  
---

### SUNSET: DECOY

A beginner-to-intermediate machine running Debian 64-bit, designed around obfuscation and misdirection. The machine uses MD5 hashes as usernames and hostname, creating an intentional rabbit hole for attackers. The primary attack path involves extracting and cracking shadow file hashes using John the Ripper, SSHing into a restricted bash shell, escaping rbash via PATH manipulation, and discovering a privilege escalation vector through a pspy process log left by the machine creator.

- **Ports:**  22 (SSH), 80 (HTTP)
- **Exploit:**  Shadow file hash cracking using John the Ripper with full /etc/shadow format — cracked password server for user 296640a3b825115a47b68fc44501c828, followed by SSH login into rbash and PATH variable manipulation to escape the restricted shell.
- **PrivEsc:**  chkrootkit 0.49 (CVE-2014-0476) local privilege escalation — root runs chkrootkit via cron job which executes /tmp/update if present. Created a malicious /tmp/update reverse shell payload, caught by a Netcat listener on Kali, resulting in a root shell.

---

### BRAINPAN-1

A medium-difficulty machine built entirely around **stack buffer overflow** exploitation. The vulnerable service (`brainpan.exe`) runs on Linux via Wine, making it a hybrid Windows/Linux target. Initial access requires developing a custom BOF exploit from scratch — fuzzing, EIP control, bad character analysis, JMP ESP return address, and shellcode injection. Post-exploitation involves a straightforward Linux privilege escalation via a sudo misconfiguration.

- **Ports:** 9999 (brainpan.exe — custom password prompt), 10000 (HTTP - Python SimpleHTTPServer 0.6)
- **Exploit:** Manual stack buffer overflow — 524 byte offset, JMP ESP at `0x311712F3`, `linux/x86/shell_reverse_tcp` shellcode via msfvenom, NOP sled, reverse shell caught on Kali
- **PrivEsc:** `sudo -l` revealed `anansi_util` — ran `sudo /home/anansi/bin/anansi_util manual man`, spawned root shell via `!bash` (GTFOBins man exploit)

---

## 🛠️ Tools Used

![Nmap](https://img.shields.io/badge/-Nmap-blue) ![Metasploit](https://img.shields.io/badge/-Metasploit-blueviolet) ![WPScan](https://img.shields.io/badge/-WPScan-red) ![CeWL](https://img.shields.io/badge/-CeWL-orange) ![GTFOBins](https://img.shields.io/badge/-GTFOBins-black) ![Nikto](https://img.shields.io/badge/-Nikto-green) ![ffuf](https://img.shields.io/badge/-ffuf-yellow) ![Immunity Debugger](https://img.shields.io/badge/-Immunity_Debugger-grey) ![msfvenom](https://img.shields.io/badge/-msfvenom-red)

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
