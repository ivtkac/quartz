---
title: How to configure exim4 with roundcube
created: 2025-12-05
tags:
  - 🦮how-to
  - ubuntu
  - exim4
  - roundcube
aliases:
lang:
---
https://wafaicloud.com/blog/setting-up-exim-for-your-linux-mail-server/

```bash
apt-get install exim4-daemon-heavy
apt install exim4 exim4-daemon-light -y
dpkg-reconfigure exim4-config
echo "This is a test email sent directly via Exim4." | mail -s "Exim4 CLI Test" testmail@email
```

https://temp-mail.org/en/

https://www.exim.org/exim-html-current/doc/html/spec_html/ch-the_dovecot_authenticator.html