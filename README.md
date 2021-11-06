Add these two hooks to `/etc/pacman.d/hooks/` and systemd-boot will be updated automatically with new enteries.

Prerequisites:
* `bootctl install` (no configuration in necesarry!)
* `mkdir /boot/$(cat /etc/machine-id)` (needed for `kernel-install` to work, see [the official documentation](https://www.freedesktop.org/software/systemd/man/kernel-install.html))

Other configuration requirements:
* None

Conflicts:
* Should not be used at the same time as [a hook to generate a new dracut image on update](https://wiki.archlinux.org/index.php/Dracut#Generate_a_new_initramfs_on_kernel_upgrade), my hook is all you need

"Problems":
* Images are not placed in `/boot/`, kernel + initrd goes to `/boot/$MACHINE-ID/$KVER/{vmlinuz,initrd}`
