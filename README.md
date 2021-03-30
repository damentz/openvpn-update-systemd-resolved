# openvpn-update-systemd-resolved
Fork of: https://aur.archlinux.org/packages/openvpn-update-systemd-resolved

## How to use

Install on Arch Linux with `makepkg -si`

On any *.ovpn file, append to the end:

```
script-security 2
up /usr/bin/update-systemd-resolved
up-restart
down /usr/bin/update-systemd-resolved
down-pre
```

Verify with `resolvectl` that your `tun0` device has the alternative DNS servers.
