# installationstuff
Some standard stuff to use on new Linux installation


# Mail

## Used pakets

mutt, msmtp, mailutils

## Installation Guide

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

# PLATZHALTER

# PLATZHALTER

# PLATZHALTER

# PLATZHALTER

# PLATZHALTER

# PLATZHALTER
