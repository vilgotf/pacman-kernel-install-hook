Add these two hooks to `/etc/pacman.d/hooks/` and systemd-boot will be updated automatically with new enteries.
Prerequisites:
* `bootctl --install` (no configuration in necesarry!)
* `mkdir /boot/$(cat /etc/machine-id)` (needed for `kernel-install` to work, see [the official documentation](https://www.freedesktop.org/software/systemd/man/kernel-install.html))
* Only tested with dracut

Other configuration requirements:
* None
