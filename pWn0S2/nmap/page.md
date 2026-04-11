::: page
# nmap {#nmap .title}

\

Starting Nmap 7.98 ( <https://nmap.org> ) at 2026-04-11 10:05 -0400

Nmap scan report for 10.10.10.100

Host is up (0.00073s latency).

Not shown: 65533 closed tcp ports (reset)

PORT STATE SERVICE VERSION

22/tcp open ssh OpenSSH 5.8p1 Debian 1ubuntu3 (Ubuntu Linux; protocol
2.0)

\| ssh-hostkey:

\| 1024 85:d3:2b:01:09:42:7b:20:4e:30:03:6d:d1:8f:95:ff (DSA)

\| 2048 30:7a:31:9a:1b:b8:17:e7:15:df:89:92:0e:cd:58:28 (RSA)

\|\_ 256 10:12:64:4b:7d:ff:6a:87:37:26:38:b1:44:9f:cf:5e (ECDSA)

80/tcp open http Apache httpd 2.2.17 ((Ubuntu))

\| http-cookie-flags:

\| /:

\| PHPSESSID:

\|\_ httponly flag not set

\|\_http-server-header: Apache/2.2.17 (Ubuntu)

\|\_http-title: Welcome to this Site!

MAC Address: 08:00:27:A1:CE:BA (Oracle VirtualBox virtual NIC)

Device type: general purpose

Running: Linux 2.6.X\|3.X

OS CPE: cpe:/o:linux:linux_kernel:2.6 cpe:/o:linux:linux_kernel:3

OS details: Linux 2.6.32 - 2.6.39, Linux 2.6.38 - 3.0

Network Distance: 1 hop

Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE

HOP RTT ADDRESS

1 0.73 ms 10.10.10.100

OS and Service detection performed. Please report any incorrect results
at <https://nmap.org/submit/> .

Nmap done: 1 IP address (1 host up) scanned in 12.87 seconds
:::
