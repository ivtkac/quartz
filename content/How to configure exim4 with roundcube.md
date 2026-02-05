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
links:
  - "[[exim4]]"
  - "[[Roundcube]]"
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

```php
$config['imap_host'] = 'localhost:143';
$config['smtp_host'] = 'localhost:25';
$config['smtp_user'] = '';
$config['smtp_pass'] = '';
$config['smtp_auth_type'] = '';

// provide an URL where a user can get support for this Roundcube installation
// PLEASE DO NOT LINK TO THE ROUNDCUBE.NET WEBSITE HERE!
$config['support_url'] = '';

// This key is used for encrypting purposes, like storing of imap password
// in the session. For historical reasons it's called DES_key, but it's used
// with any configured cipher_method (see below).
// For the default cipher_method a required key length is 24 characters.
$config['des_key'] = 't1J1ObYUB9Y3DoMLPZc0tj8K';

// ----------------------------------
// PLUGINS
// ----------------------------------
// List of active plugins (in plugins/ directory)
$config['plugins'] = ['acl', 'additional_message_headers', 'archive', 'attachment_reminder', 'autologon', 'autologout', 'debug_logger', 'emoticons', 'enigma', 'example_addressbook',  'help', 'hide_blockquote', 'http_authentication', 'identicon', 'identity_select', 'jqueryui', 'krb_authentication', 'managesieve', 'markasjunk', 'new_user_dialog', 'new_user_identity', 'newmail_notifier', 'password', 'reconnect', 'redundant_attachments', 'show_additional_headers', 'squirrelmail_usercopy', 'subscriptions_option', 'userinfo', 'vcard_attachments', 'virtuser_file', 'virtuser_query', 'zipdownload'];

// Make use of the built-in spell checker.
$config['enable_spellcheck'] = true;

```

## /etc/exim4/update-exim4.conf.conf

```php
dc_eximconfig_configtype='internet'
dc_other_hostnames=''
dc_local_interfaces='127.0.0.1; 91.99.226.119'
dc_readhost='mail.example.com'
dc_relay_domains=''
dc_minimaldns='false'
dc_relay_nets=''
dc_smarthost='mail.example.com'
CFILEMODE='644'
dc_use_split_config='false'
dc_hide_mailname='true'
dc_mailname_in_oh='true'
dc_localdelivery='maildir_home'
~                                
```

## /etc/exim4/conf.d/auth/30_exim4-config_examples

```ini
dovecot_plain_server:
   driver = dovecot
   public_name = PLAIN
   server_socket = /var/spool/exim4/dovecot.auth-client
   server_set_id = $auth1
   .ifndef AUTH_SERVER_ALLOW_NOTLS_PASSWORDS
   server_advertise_condition = ${if eq{$tls_in_cipher}{}{}{*}}
   .endif
```

## /etc/dovecot/conf.d/10-master.conf

```php
service auth {
	...
  unix_listener /var/spool/exim4/dovecot.auth-client {
    mode = 0660
    user = Debian-exim
  }
	...
}
```

## Troubleshooting

https://wiki.debian.org/PkgExim4UserFAQ#I_get_the_error_.22Mailing_to_remote_domains_not_supported.22

## Cheatsheet

https://bradthemad.org/tech/notes/exim_cheatsheet.php