::: page
# nmap {#nmap .title}

\

Starting Nmap 7.98 ( <https://nmap.org> ) at 2026-04-06 20:33 -0400

Nmap scan report for 192.168.56.103

Host is up (0.00072s latency).

Not shown: 65532 filtered tcp ports (no-response)

PORT STATE SERVICE VERSION

22/tcp closed ssh

80/tcp open http Apache httpd

\|\_http-server-header: Apache

\|\_http-title: Site doesn\'t have a title (text/html).

443/tcp open ssl/http Apache httpd

\|\_ssl-date: TLS randomness does not represent time

\|\_http-server-header: Apache

\| ssl-cert: Subject:
commonName=[www.example.com](http://www.example.com)

\| Not valid before: 2015-09-16T10:45:03

\|\_Not valid after: 2025-09-13T10:45:03

\|\_http-title: Site doesn\'t have a title (text/html).

MAC Address: 08:00:27:E8:69:40 (Oracle VirtualBox virtual NIC)

Aggressive OS guesses: Linux 3.10 - 4.11 (98%), Linux 3.2 - 4.14 (94%),
Amazon Fire TV (93%), Linux 3.2 - 3.8 (93%), Linux 3.13 - 4.4 (93%),
Linux 3.18 (93%), Linux 3.13 or 4.2 (92%), Linux 4.4 (92%), Synology
DiskStation Manager 7.1 (Linux 4.4) (92%), Linux 2.6.32 - 3.13 (91%)

No exact OS matches for host (test conditions non-ideal).

Network Distance: 1 hop

TRACEROUTE

HOP RTT ADDRESS

1 0.71 ms 192.168.56.103

OS and Service detection performed. Please report any incorrect results
at <https://nmap.org/submit/> .

Nmap done: 1 IP address (1 host up) scanned in 109.04 seconds
:::
