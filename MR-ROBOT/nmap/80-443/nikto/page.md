::: page
# nikto {#nikto .title}

\

- Nikto v2.6.0

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\+ Your Nikto installation is out of date.

\+ Target IP: 192.168.56.103

\+ Target Hostname: 192.168.56.103

\+ Target Port: 80

\+ Platform: Unknown

\+ Start Time: 2026-04-07 12:52:43 (GMT-4)

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\+ Server: Apache

\+ \[999986\] /server-status: Retrieved x-powered-by header: PHP/5.5.29.

\+ No CGI Directories found (use \'-C all\' to force check all possible
dirs). CGI tests skipped.

\+ \[999100\] /index: Uncommon header(s) \'tcn\' found, with contents:
list.

\+ \[999965\] /index: Apache mod_negotiation is enabled with MultiViews,
which allows attackers to easily brute force file names. The following
alternatives for \'index\' were found: index.html, index.php. See:
<http://www.wisec.it/sectou.php?id=4698ebdc59d15,https://exchange.xforce.ibmcloud.com/vulnerabilities/8275>

\+ \[013587\] /: Suggested security header missing: referrer-policy.
See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy>

\+ \[013587\] /: Suggested security header missing:
x-content-type-options. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Content-Type-Options>

\+ \[013587\] /: Suggested security header missing:
content-security-policy. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP>

\+ \[013587\] /: Suggested security header missing: permissions-policy.
See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Permissions-Policy>

\+ \[013587\] /: Suggested security header missing:
strict-transport-security. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security>

\+ \[001820\] /readme: This might be interesting.

\+ \[000427\] /image/: Link header(s) found with value(s):
\<<http://192.168.56.103/?p=23>\>; rel=shortlink. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Link>

\+ \[003127\]
/phpmyadmin/export.php?what=../../../../../../../..//etc/hosts%00:
phpMyAdmin is vulnerable to a directory traversal attack. See:
<https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2004-0129>

\+ \[003127\]
/phpmyadmin/export.php?what=..\\..\\..\\..\\..\\..\\..\\..\\\\Windows\\win.ini%00:
phpMyAdmin is vulnerable to a directory traversal attack. See:
<https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2004-0129>

\+ \[006184\] /wp-links-opml.php: This WordPress script reveals the
installed version.

\+ \[006186\] /license.txt: License file found may identify site
software.

\+ \[006230\] /admin/index.html: Admin login page/section found.

\+ \[95\] /wp-login/: Cookie wordpress_test_cookie created without the
httponly flag. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies>

\+ \[006415\] /wp-login/: Admin login page/section found.

\+ \[006668\] /wp-login.php: WordPress login found.

\+ \[999979\] <http://100.100.100.200/latest/meta-data/:> IP address
found in the \'x-pingback\' header. The IP is \"100.100.100.200\". See:
<https://portswigger.net/kb/issues/00600300_private-ip-addresses-disclosed>

\+ \[999979\] <http://100.100.100.200/latest/meta-data/:> IP address
found in the \'location\' header. The IP is \"100.100.100.200\". See:
<https://portswigger.net/kb/issues/00600300_private-ip-addresses-disclosed>

\+ \[007352\] /: The X-Content-Type-Options header is not set. This
could allow the user agent to render the content of the site in a
different fashion to the MIME type. See:
<https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/>

\+ 8238 requests: 16 errors and 21 items reported on the remote host

\+ End Time: 2026-04-07 13:00:04 (GMT-4) (441 seconds)

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--
:::
