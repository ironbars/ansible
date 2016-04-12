`/etc/ansible/general/files/`
============================
<!---
The tasks here should be to: 

1. Copy `home/user/bash_profile` to `~/.bash_profile` on the remote machine
2. Copy `home/user/bashrc` to `~/.bashrc` on the remote machine
3. Copy the `home/user/config/bash` directory whole to `~/.config/bash`
4. Copy the `home/user/config/lxterminal` directory whole to ~/.config/lxterminal`
5. Copy the `home/user/config/gtk-3.0` directory whole to `~/.config/gtk-3.0`
-->

This directory should be viewed as a virtual '/'.  Thus, copy files in each 
subdirectory under it to the appropriate place on the remote machine.

For example, place `home/user/bash_profile` to `~/.bash_profile` on the remote 
machine.  Place `etc/lightdm/lightdm.conf` at `/etc/lightdm/lightdm.conf` on 
the remote machine, etc.
