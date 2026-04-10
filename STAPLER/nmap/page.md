::: page
# nmap {#nmap .title}

\

Starting Nmap 7.98 ( <https://nmap.org> ) at 2026-04-10 07:29 -0400

Nmap scan report for 192.168.56.104

Host is up (0.00071s latency).

Not shown: 65523 filtered tcp ports (no-response)

PORT STATE SERVICE VERSION

20/tcp closed ftp-data

21/tcp open ftp vsftpd 2.0.8 or later

\| ftp-syst:

\| STAT:

\| FTP server status:

\| Connected to 192.168.56.1

\| Logged in as ftp

\| TYPE: ASCII

\| No session bandwidth limit

\| Session timeout in seconds is 300

\| Control connection is plain text

\| Data connections will be plain text

\| At session startup, client count was 2

\| vsFTPd 3.0.3 - secure, fast, stable

\|\_End of status

\| ftp-anon: Anonymous FTP login allowed (FTP code 230)

\|\_Can\'t get directory listing: PASV failed: 550 Permission denied.

22/tcp open ssh OpenSSH 7.2p2 Ubuntu 4 (Ubuntu Linux; protocol 2.0)

\| ssh-hostkey:

\| 2048 81:21:ce:a1:1a:05:b1:69:4f:4d:ed:80:28:e8:99:05 (RSA)

\| 256 5b:a5:bb:67:91:1a:51:c2:d3:21:da:c0:ca:f0:db:9e (ECDSA)

\|\_ 256 6d:01:b7:73:ac:b0:93:6f:fa:b9:89:e6:ae:3c:ab:d3 (ED25519)

53/tcp open domain dnsmasq 2.75

\| dns-nsid:

\|\_ bind.version: dnsmasq-2.75

80/tcp open http PHP cli server 5.5 or later

\|\_http-title: 404 Not Found

123/tcp closed ntp

137/tcp closed netbios-ns

138/tcp closed netbios-dgm

139/tcp open netbios-ssn Samba smbd 4.3.9-Ubuntu (workgroup: WORKGROUP)

666/tcp open pkzip-file .ZIP file

\| fingerprint-strings:

\| NULL:

\| message2.jpgUT

\| QWux

\| \"DL\[E

\| #;3\[

\| \\xf6

\| u(\[r

\| qYQq

\| Y\_?n2

\| 3&M\~{

\| 9-a)T

\| L}AJ

\|\_ .npy.9

3306/tcp open mysql MySQL 5.7.12-0ubuntu1

\| mysql-info:

\| Protocol: 10

\| Version: 5.7.12-0ubuntu1

\| Thread ID: 7

\| Capabilities flags: 63487

\| Some Capabilities: DontAllowDatabaseTableColumn, Speaks41ProtocolOld,
SupportsTransactions, ConnectWithDatabase, SupportsLoadDataLocal,
Support41Auth, Speaks41ProtocolNew, LongPassword,
IgnoreSpaceBeforeParenthesis, LongColumnFlag, InteractiveClient,
ODBCClient, SupportsCompression, FoundRows, IgnoreSigpipes,
SupportsMultipleResults, SupportsMultipleStatments, SupportsAuthPlugins

\| Status: Autocommit

\| Salt: \\x14+QRb\\x07\^\\x13lD \\x0F\|F+\~c\^\\x15q

\|\_ Auth Plugin Name: mysql_native_password

12380/tcp open http Apache httpd 2.4.18 ((Ubuntu))

\|\_http-server-header: Apache/2.4.18 (Ubuntu)

\|\_http-title: Site doesn\'t have a title (text/html).

1 service unrecognized despite returning data. If you know the
service/version, please submit the following fingerprint at
<https://nmap.org/cgi-bin/submit.cgi?new-service> :

SF-Port666-TCP:V=7.98%I=7%D=4/10%Time=69D8DF55%P=x86_64-pc-linux-gnu%r(NUL

SF:L,10F8,\"PK\\x03\\x04\\x14\\0\\x02\\0\\x08\\0d\\x80\\xc3Hp\\xdf\\x15\\x81\\xaa,\\0\\0\\x1

SF:52\\0\\0\\x0c\\0\\x1c\\0message2\\.jpgUT\\t\\0\\x03\\+\\x9cQWJ\\x9cQWux\\x0b\\0\\x01\\x0

SF:4\\xf5\\x01\\0\\0\\x04\\x14\\0\\0\\0\\xadz\\x0bT\\x13\\xe7\\xbe\\xefP\\x94\\x88\\x88A@\\xa

SF:2\\x20\\x19\\xabUT\\xc4T\\x11\\xa9\\x102\>\\x8a\\xd4RDK\\x15\\x85Jj\\xa9\\\"DL\\\[E\\xa2\\

SF:x0c\\x19\\x140\<\\xc4\\xb4\\xb5\\xca\\xaen\\x89\\x8a\\x8aV\\x11\\x91W\\xc5H\\x20\\x0f\\x

SF:b2\\xf7\\xb6\\x88\\n\\x82@%\\x99d\\xb7\\xc8#;3\\\[\\r\_\\xcddr\\x87\\xbd\\xcf9\\xf7\\xaeu

SF:\\xeeY\\xeb\\xdc\\xb3oX\\xacY\\xf92\\xf3e\\xfe\\xdf\\xff\\xff\\xff=2\\x9f\\xf3\\x99\\xd

SF:3\\x08y}\\xb8a\\xe3\\x06\\xc8\\xc5\\x05\\x82\>\`\\xfe\\x20\\xa7\\x05:\\xb4y\\xaf\\xf8\\xa

SF:0\\xf8\\xc0\\\^\\xf1\\x97sC\\x97\\xbd\\x0b\\xbd\\xb7nc\\xdc\\xa4I\\xd0\\xc4\\+j\\xce\\\[\\x

SF:87\\xa0\\xe5\\x1b\\xf7\\xcc=,\\xce\\x9a\\xbb\\xeb\\xeb\\xdds\\xbf\\xde\\xbd\\xeb\\x8b\\x

SF:f4\\xfdis\\x0f\\xeeM\\?\\xb0\\xf4\\x1f\\xa3\\xcceY\\xfb\\xbe\\x98\\x9b\\xb6\\xfb\\xe0\\x

SF:dc\\\]sS\\xc5bQ\\xfa\\xee\\xb7\\xe7\\xbc\\x05AoA\\x93\\xfe9\\xd3\\x82\\x7f\\xcc\\xe4\\xd

SF:5\\x1dx\\xa2O\\x0e\\xdd\\x994\\x9c\\xe7\\xfe\\x871\\xb0N\\xea\\x1c\\x80\\xd63w\\xf1\\xa

SF:f\\xbd&&q\\xf9\\x97\'i\\x85fL\\x81\\xe2\\\\\\xf6\\xb9\\xba\\xcc\\x80\\xde\\x9a\\xe1\\xe2:

SF:\\xc3\\xc5\\xa9\\x85\`\\x08r\\x99\\xfc\\xcf\\x13\\xa0\\x7f{\\xb9\\xbc\\xe5:i\\xb2\\x1bk\\

SF:x8a\\xfbT\\x0f\\xe6\\x84\\x06/\\xe8-\\x17W\\xd7\\xb7&\\xb9N\\x9e\<\\xb1\\\\\\.\\xb9\\xcc\\

SF:xe7\\xd0\\xa4\\x19\\x93\\xbd\\xdf\\\^\\xbe\\xd6\\xcdg\\xcb\\.\\xd6\\xbc\\xaf\\\|W\\x1c\\xfd

SF:\\xf6\\xe2\\x94\\xf9\\xebj\\xdbf\~\\xfc\\x98x\'\\xf4\\xf3\\xaf\\x8f\\xb9O\\xf5\\xe3\\xcc\\

SF:x9a\\xed\\xbf\`a\\xd0\\xa2\\xc5KV\\x86\\xad\\n\\x7fou\\xc4\\xfa\\xf7\\xa37\\xc4\\\|\\xb0\\

SF:xf1\\xc3\\x84O\\xb6nK\\xdc\\xbe#\\)\\xf5\\x8b\\xdd{\\xd2\\xf6\\xa6g\\x1c8\\x98u\\(\\\[r\\

SF:xf8H\~A\\xe1qYQq\\xc9w\\xa7\\xbe\\?}\\xa6\\xfc\\x0f\\?\\x9c\\xbdTy\\xf9\\xca\\xd5\\xaak

SF:\\xd7\\x7f\\xbcSW\\xdf\\xd0\\xd8\\xf4\\xd3\\xddf\\xb5F\\xabk\\xd7\\xff\\xe9\\xcf\\x7fy\\

SF:xd2\\xd5\\xfd\\xb4\\xa7\\xf7Y\_\\?n2\\xff\\xf5\\xd7\\xdf\\x86\\\^\\x0c\\x8f\\x90\\x7f\\x7f

SF:\\xf9\\xea\\xb5m\\x1c\\xfc\\xfef\\\"\\.\\x17\\xc8\\xf5\\?B\\xff\\xbf\\xc6\\xc5,\\x82\\xcb\\

SF:\[\\x93&\\xb9NbM\\xc4\\xe5\\xf2V\\xf6\\xc4\\t3&M\~{\\xb9\\x9b\\xf7\\xda-\\xac\\\]\_\\xf9\\x

SF:cc\\\[qt\\x8a\\xef\\xbao/\\xd6\\xb6\\xb9\\xcf\\x0f\\xfd\\x98\\x98\\xf9\\xf9\\xd7\\x8f\\xa

SF:7\\xfa\\xbd\\xb3\\x12\_@N\\x84\\xf6\\x8f\\xc8\\xfe{\\x81\\x1d\\xfb\\x1fE\\xf6\\x1f\\x81\\

SF:xfd\\xef\\xb8\\xfa\\xa1i\\xae\\.L\\xf2\\\\g@\\x08D\\xbb\\xbfp\\xb5\\xd4\\xf4Ym\\x0bI\\x9

SF:6\\x1e\\xcb\\x879-a\\)T\\x02\\xc8\\\$\\x14k\\x08\\xae\\xfcZ\\x90\\xe6E\\xcb\<C\\xcap\\x8f

SF:\\xd0\\x8f\\x9fu\\x01\\x8dvT\\xf0\'\\x9b\\xe4ST%\\x9f5\\x95\\xab\\rSWb\\xecN\\xfb&\\xf4

SF:\\xed\\xe3v\\x13O\\xb73A#\\xf0,\\xd5\\xc2\\\^\\xe8\\xfc\\xc0\\xa7\\xaf\\xab4\\xcfC\\xcd\\

SF:x88\\x8e}\\xac\\x15\\xf6\~\\xc4R\\x8e\`wT\\x96\\xa8KT\\x1cam\\xdb\\x99f\\xfb\\n\\xbc\\xb

SF:cL}AJ\\xe5H\\x912\\x88\\(O\\0k\\xc9\\xa9\\x1a\\x93\\xb8\\x84\\x8fdN\\xbf\\x17\\xf5\\xf0

SF:\\.npy\\.9\\x04\\xcf\\x14\\x1d\\x89Rr9\\xe4\\xd2\\xae\\x91#\\xfbOg\\xed\\xf6\\x15\\x04\\

SF:xf6\~\\xf1\\\]V\\xdcBGu\\xeb\\xaa=\\x8e\\xef\\xa4HU\\x1e\\x8f\\x9f\\x9bI\\xf4\\xb6GTQ\\x

SF:f3\\xe9\\xe5\\x8e\\x0b\\x14L\\xb2\\xda\\x92\\x12\\xf3\\x95\\xa2\\x1c\\xb3\\x13\\\*P\\x11\\

SF:?\\xfb\\xf3\\xda\\xcaDfv\\x89\`\\xa9\\xe4k\\xc4S\\x0e\\xd6P0\");

MAC Address: 08:00:27:03:99:94 (Oracle VirtualBox virtual NIC)

No exact OS matches for host (If you know what OS is running on it, see
<https://nmap.org/submit/> ).

TCP/IP fingerprint:

OS:SCAN(V=7.98%E=4%D=4/10%OT=21%CT=20%CU=30762%PV=Y%DS=1%DC=D%G=Y%M=080027%

OS:TM=69D8DF8A%P=x86_64-pc-linux-gnu)SEQ(SP=101%GCD=1%ISR=103%TI=Z%CI=I%TS=

OS:8)SEQ(SP=102%GCD=1%ISR=10A%TI=Z%CI=I%TS=8)SEQ(SP=105%GCD=1%ISR=107%TI=Z%

OS:CI=I%TS=8)SEQ(SP=107%GCD=1%ISR=10B%TI=Z%CI=I%TS=8)SEQ(SP=108%GCD=1%ISR=1

OS:0F%TI=Z%CI=I%TS=8)OPS(O1=M5B4ST11NW7%O2=M5B4ST11NW7%O3=M5B4NNT11NW7%O4=M

OS:5B4ST11NW7%O5=M5B4ST11NW7%O6=M5B4ST11)WIN(W1=7120%W2=7120%W3=7120%W4=712

OS:0%W5=7120%W6=7120)ECN(R=Y%DF=Y%T=40%W=7210%O=M5B4NNSNW7%CC=Y%Q=)T1(R=Y%D

OS:F=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R=Y%DF=Y%T=40%W=0%S=A%A=

OS:Z%F=R%O=%RD=0%Q=)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=Y%DF

OS:=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)T7(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=

OS:%RD=0%Q=)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G

OS:)IE(R=N)

Network Distance: 1 hop

Service Info: Host: RED; OS: Linux; CPE: cpe:/o:linux:linux_kernel

Host script results:

\| smb2-time:

\| date: 2026-04-10T11:30:49

\|\_ start_date: N/A

\| smb-security-mode:

\| account_used: guest

\| authentication_level: user

\| challenge_response: supported

\|\_ message_signing: disabled (dangerous, but default)

\| smb2-security-mode:

\| 3.1.1:

\|\_ Message signing enabled but not required

\| smb-os-discovery:

\| OS: Windows 6.1 (Samba 4.3.9-Ubuntu)

\| Computer name: red

\| NetBIOS computer name: RED\\x00

\| Domain name: \\x00

\| FQDN: red

\|\_ System time: 2026-04-10T12:30:49+01:00

\|\_clock-skew: mean: -20m02s, deviation: 34m38s, median: -3s

\|\_nbstat: NetBIOS name: RED, NetBIOS user: \<unknown\>, NetBIOS MAC:
\<unknown\> (unknown)

TRACEROUTE

HOP RTT ADDRESS

1 0.71 ms 192.168.56.104

OS and Service detection performed. Please report any incorrect results
at <https://nmap.org/submit/> .

Nmap done: 1 IP address (1 host up) scanned in 141.81 seconds
:::
