# Debian install tweaks

Things I like to adjust on new installs at home:

- update `/etc/initramfs-tools/initramfs.conf`: `MODULES=dep`
- use full-disc encryption, possible with auto-login to save double-login
- install and configure efihelper for efistub boot
- remove jre, openoffice, thunderbird
