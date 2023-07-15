# PAM (pluggable authentication module)

Module that handles users and their accesses. It is highly customizable. 

`cd /etc/pam.d/`
`ls`
`cat common-password`

This file specifies some limitations on users' passwords requirements, such as password length, allowed characters used in the password, if special characters are allowed or not, etc.

For keeping data of 1000 users PAM is not very effective. Instead of it, **active directories (AD)** can be used.

# LDAP (Lightweight directory authentication protocol)

The software is called openldap. LDAP is a protocol (which is different from software).

AD (Active directory) - developed by Microsoft, paid software, expensive, works only Windows to(->) Windows
IDM (Identity manager) - developed by Red Hat, also paid enterprise software. Works 
  - Linux -> Linux
  - Linux -> Windows
  - Windows -> Linux
openLdap - free software (for Linux/Unix), works Windows -> Linux, also can work Linux -> Linux, but it's harder to configure
Winbind - free software by Samba (for Linux/Unix)
IBM Directory - developed by IBM Corporation, has free and paid versions

`sudo su -`
`wall`  - broadcast a message to all users

![[Screenshot 2023-07-15 at 16.50.41.png]]

`write sergey` - write a message to *sergey* user
(press Ctrl+D when finished)

