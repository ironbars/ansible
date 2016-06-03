Post-install Tasks - Common
===========================

The following tasks should be performed after a new machine is provisioned 
using Ansible.  This consists mainly of installing AUR packages and configuring 
them.  The AUR is not well suited to automation; many packages require manual 
intervention.  It is for this reason that (for now), installation of software
from the AUR must be performed manually.

Install AUR Packages
--------------------

### All ###
* cower
* pacaur
* google-chrome
* vim-pathogen
* montecarlo-font
* ttf-monaco
* dropbox
* nvpy-git
    * Dependency: tk (in official repos - use pacman to install)
    * Dependency: python2-setuptools (in official repos - use pacman to install)
* xss-lock

### General ###
* numix-themes-blue
* numix-themes-darkblue
* numix-themes-electric
* numix-frost-themes
* numix-icon-theme-git
* numix-bevel-icon-theme-git
* numix-shine-icon-theme-git

### Development ###
* i3blocks
* gtk-theme-arc
* moka-icon-theme-git
    * Dependency: faba-icon-theme-git
    * Dependency: faba-mono-icons-git

Window Manager Configuraton (Openbox) 
-------------------------------------

This section is for "general" machines.

1. Run `lxappearance` and set the following configurations:

    * Widget theme: Numix Frost (or Numix Blue, if Frost unavailable)
    * Font: Source Sans Pro 10
    * Icon theme: Numix

2. (Openbox) - run `obconf` and set the following configurations:

    * Theme: Numix Frost (or Numix Blue, if Frost unavailable)

Window Manager Configuration (i3)
---------------------------------

This section is for "development" machines.

1. Run `lxappearance` and set the following configurations:

    * Widget theme: Arc-Darker
    * Font: Source Sans Pro 10
    * Icon theme: Flattr

2. (i3) - this should mostly be taken care of by the copied config files.
   For AUR programs:

    * In the `~/.config/i3/config`, uncomment the `xss-lock` and `i3blocks`
      lines after these programs are installed.

Other Manual Configuration
--------------------------

1. After installing Dropbox, be sure to start the service as the window maanger
   starts.

    * Openbox: add `dropbox &` to `~/.config/openbox/autostart`.
    * i3: add `exec dropbox` to the end of `~/.config/i3/config`.

   Could also be started as a system service using `systemctl enable dropbox.service`.

2. It may be necessary to manually set the terminal transparency, if LXTerminal
   is being used.  Right click in the terminal window, choose "Preferences", and
   set the opacity as desired.

3. For Chrome:

    * Go to chrome://settings and click "Use GTK+ theme"
    * Add AdBlock to Chrome
    * Add Vimium to Chrome

   Alternatively, this can all be done by signing in to Chrome.

4. Add a sane symlink to the Chrome executable (as root). Like so:

   `ln -s /usr/bin/google-chrome-stable /usr/bin/chrome`

   Also, add a symlink for other programs to open the browser:

   `ln -s /usr/bin/google-chrome-stable /usr/bin/google-chrome`

5. As root, edit `/etc/lightdm/lightdm-gtk-greeter.conf`.

    * `background=/etc/lightdm/backgrounds/Army-Samurai-Wallpaper-HD.jpg`
    * `theme-name=Numix-Frost` (Openbox/general)
    * `theme-name=Arc-Darker` (i3/development)
    * `font-name=Source Sans Pro 10`
    * `xft-antialias=true`

