# Check "xca-cert" - Overview

If you are using XCA by Christian Hohnstädt (an _application that is intended for creating and managing X.509 certificates, certificate requests, RSA, DSA and EC private keys, Smart-cards and CRLs_) with ["Remote Databases" feature enabled](https://hohnstaedt.de/xca/index.php/documentation/remote-databases), this plugin lets you check the expiration date of any certificate within those XCA MySQL/MariaDB databases. CRLs are also taken into account.

We recommend to run this check direclty on your database host, and just once a day.


# Installation and Usage

Requirements:
* Python2 module `mysql.connector`

```bash
./xca-cert --hostname localhost --database xca --username dbuser --password dbpass --prefix xca_prefix_ --warning 14 --critical 5 
./xca-cert --help
```


# States

* WARN or CRIT if a certificate expires within a given threshold.


# Perfdata

There is no perfdata.


# Known Issues and Limitations

* Works with MySQL/MariaDB backend only, although XCA is supporting PostgreSQL as well.


# Credits, License

* Authors: [Linuxfabrik GmbH, Zurich](https://www.linuxfabrik.ch)
* License: The Unlicense, see LICENSE file.