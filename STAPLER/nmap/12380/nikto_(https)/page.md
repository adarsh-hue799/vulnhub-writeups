::: page
# nikto (https) {#nikto-https .title}

\

- Nikto v2.6.0

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\+ Your Nikto installation is out of date.

\+ Target IP: 192.168.56.104

\+ Target Hostname: 192.168.56.104

\+ Target Port: 12380

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\+ SSL Info: Subject: /C=UK/ST=Somewhere in the middle of
nowhere/L=Really, what are you meant to put here?/O=Initech/OU=Pam: I
give up. no idea what to put
here./CN=Red.Initech/emailAddress=pam@red.localhost

CN: Red.Initech

Ciphers: ECDHE-RSA-AES256-GCM-SHA384

Issuer: /C=UK/ST=Somewhere in the middle of nowhere/L=Really, what are
you meant to put here?/O=Initech/OU=Pam: I give up. no idea what to put
here./CN=Red.Initech/emailAddress=pam@red.localhost

\+ Platform: Unknown

\+ Start Time: 2026-04-10 09:48:00 (GMT-4)

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\+ Server: Apache/2.4.18 (Ubuntu)

\+ \[999100\] /: Uncommon header(s) \'dave\' found, with contents:
Soemthing doesn\'t look right here.

\+ No CGI Directories found (use \'-C all\' to force check all possible
dirs). CGI tests skipped.

\+ \[999996\] /robots.txt: contains 2 entries which should be manually
viewed. See:
<https://developer.mozilla.org/en-US/docs/Glossary/Robots.txt>

\+ \[013587\] /: Suggested security header missing: permissions-policy.
See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Permissions-Policy>

\+ \[013587\] /: Suggested security header missing:
content-security-policy. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP>

\+ \[013587\] /: Suggested security header missing:
x-content-type-options. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Content-Type-Options>

\+ \[013587\] /: Suggested security header missing:
strict-transport-security. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security>

\+ \[013587\] /: Suggested security header missing: referrer-policy.
See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy>

\+ \[999993\] /: Hostname \'192.168.56.104\' does not match certificate
names (CN: Red.Initech, SAN: none). See:
<https://cwe.mitre.org/data/definitions/297.html>

\+ \[600050\] Apache/2.4.18 appears to be outdated (current is at least
2.4.66).

\+ \[999990\] OPTIONS: Allowed HTTP Methods: POST, OPTIONS, GET, HEAD .

\+ \[999100\] /phpmyadmin/changelog.php: Uncommon header(s)
\'x-ob_mode\' found, with contents: 1.

\+ \[003584\] /icons/README: Apache default file found. See:
<https://www.vntweb.co.uk/apache-restricting-access-to-iconsreadme/>

\+ /: No creds found for realm \'phpMyAdmin Setup\'
:::
