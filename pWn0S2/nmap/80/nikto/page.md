::: page
# nikto {#nikto .title}

\

- Nikto v2.6.0

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\+ Your Nikto installation is out of date.

\+ Target IP: 10.10.10.100

\+ Target Hostname: 10.10.10.100

\+ Target Port: 80

\+ Platform: Unknown

\+ Start Time: 2026-04-11 14:43:22 (GMT-4)

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\+ Server: Apache/2.2.17 (Ubuntu)

\+ \[95\] /: Cookie PHPSESSID created without the httponly flag. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies>

\+ \[999986\] /: Retrieved x-powered-by header: PHP/5.3.5-1ubuntu7.

\+ \[750500\] /icons/: Directory indexing found.

\+ No CGI Directories found (use \'-C all\' to force check all possible
dirs). CGI tests skipped.

\+ \[999100\] /index: Uncommon header(s) \'tcn\' found, with contents:
list.

\+ \[999965\] /index: Apache mod_negotiation is enabled with MultiViews,
which allows attackers to easily brute force file names. The following
alternatives for \'index\' were found: index.php. See:
<http://www.wisec.it/sectou.php?id=4698ebdc59d15,https://exchange.xforce.ibmcloud.com/vulnerabilities/8275>

\+ \[013587\] /: Suggested security header missing:
x-content-type-options. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Content-Type-Options>

\+ \[013587\] /: Suggested security header missing:
strict-transport-security. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security>

\+ \[013587\] /: Suggested security header missing:
content-security-policy. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP>

\+ \[013587\] /: Suggested security header missing: referrer-policy.
See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy>

\+ \[013587\] /: Suggested security header missing: permissions-policy.
See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Permissions-Policy>

\+ \[600050\] Apache/2.2.17 appears to be outdated (current is at least
2.4.66).

\+ \[600625\] PHP/5.3.5-1ubuntu7 appears to be outdated (current is at
least 8.5.1).

\+ \[999967\] /: Web Server returns a valid response with junk HTTP
methods which may cause false positives.

\+ \[001384\] /?=PHPB8B5F2A0-3C92-11d3-A3A9-4C7B08C10000: PHP Easter
Eggs reveals potentially sensitive information via HTTP requests that
contain specific QUERY strings. See:
<https://labs.detectify.com/writeups/do-you-dare-to-show-your-php-easter-egg/>

\+ \[001385\] /?=PHPE9568F36-D428-11d2-A769-00AA001ACF42: PHP Easter Egg
reveals potentially sensitive information via HTTP requests that contain
specific QUERY strings. See:
<https://labs.detectify.com/writeups/do-you-dare-to-show-your-php-easter-egg/>

\+ \[001386\] /?=PHPE9568F34-D428-11d2-A769-00AA001ACF42: PHP Easter Egg
reveals potentially sensitive information via HTTP requests that contain
specific QUERY strings. See:
<https://labs.detectify.com/writeups/do-you-dare-to-show-your-php-easter-egg/>

\+ \[001387\] /?=PHPE9568F35-D428-11d2-A769-00AA001ACF42: PHP Easter Egg
reveals potentially sensitive information via HTTP requests that contain
specific QUERY strings. See:
<https://labs.detectify.com/writeups/do-you-dare-to-show-your-php-easter-egg/>

\+ \[750500\] /includes/: Directory indexing found.

\+ \[001702\] /includes/: This might be interesting.

\+ \[750510\] /info/: Output from the phpinfo() function was found.

\+ \[001704\] /info/: This might be interesting.

\+ \[001736\] /login/: This might be interesting.

\+ \[001823\] /register/: This might be interesting.

\+ \[750510\] /info.php: Output from the phpinfo() function was found.

\+ \[002989\] /info.php: PHP is installed, and a test script which runs
phpinfo() was found. This gives a lot of system information. See:
CWE-552

\+ \[999984\] /icons/README: Server may leak inodes via ETags, header
found with file /icons/README, inode: 1311031, size: 5108, mtime: Tue
Aug 28 06:48:10 2007. See:
<https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2003-1418>

\+ \[003584\] /icons/README: Apache default file found. See:
<https://www.vntweb.co.uk/apache-restricting-access-to-iconsreadme/>

\+ \[005170\] /info.php?file=<https://cirt.net/public/rfiinc.txt:>
Remote File Inclusion (RFI) from RSnake\'s RFI list. See:
<https://gist.github.com/mubix/5d269c686584875015a2>

\+ \[006333\] /login.php: Admin login page/section found.

\+ \[007342\] /: X-Frame-Options header is deprecated and was replaced
with the Content-Security-Policy HTTP header with the frame-ancestors
directive. See:
<https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/X-Frame-Options>

\+ \[007352\] /: The X-Content-Type-Options header is not set. This
could allow the user agent to render the content of the site in a
different fashion to the MIME type. See:
<https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/>

\+ 8176 requests: 16 errors and 31 items reported on the remote host

\+ End Time: 2026-04-11 14:48:53 (GMT-4) (331 seconds)

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\+ 1 host(s) tested
:::
