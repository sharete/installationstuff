# installationstuff
Some standard stuff to use on new Linux installation


# Mail

## Used pakets

mutt, msmtp, mailutils, lynx

## Installation Guide

# E-Mails senden

1. Konfigurationsdatei für msmtp erstellen

```bash
nano ~/.msmtprc
```

2. Parameter hinzufügen

```bash
account default
host smtp.deinprovider.com
port 587
from deineemail@deinprovider.com
auth on
user deineemail@deinprovider.com
password deinpasswort
tls on
tls_starttls on
tls_trust_file /etc/ssl/certs/ca-certificates.crt

logfile ~/.msmtp.log
```

3. Berechtigungen ändern

```bash
chmod 600 ~/.msmtprc
```

# E-Mails empfangen
Mutt wird verwendet, um Mails zu empfangen.

1. Parameter in .muttrc hinzufügen

```bash
set imap_user = "emailadresse"
set imap_pass = "psswd"
set folder = "imaps://imap.strato.de/"
set spoolfile = "+INBOX"
set record = "+Sent"
set postponed = "+Drafts"
set ssl_starttls = yes
set ssl_force_tls = yes
set certificate_file = /etc/ssl/certs/ca-certificates.crt
set sendmail="/usr/bin/msmtp"
set use_from=yes
set realname="name"
set envelope_from=yes
set from="emailadresse"

auto_view text/html
alternative_order text/plain text/enriched text/html
```
2. Parameter in .msmtprc hinzufügen

```bash
account default
host smtp.strato.de
port 465
from mailadresse
auth on
user mailadresse
password deinpw
tls on
tls_starttls off
tls_trust_file /etc/ssl/certs/ca-certificates.crt

logfile ~/.msmtp.log
```


# PLATZHALTER

# PLATZHALTER

# PLATZHALTER

# PLATZHALTER

# PLATZHALTER

# PLATZHALTER
