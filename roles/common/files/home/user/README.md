Post-install Tasks - Common
===========================

The following tasks should be performed after a new machine is provisioned 
using Ansible.  This consists mainly of installing AUR pakcages and configuring 
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

### General ###
* numix-themes-blue
* numix-themes-darkblue
* numix-themes-electric
* numix-frost-themes
* numix-icon-theme-git
* numix-bevel-icon-theme-git
* numix-shine-icon.theme-git

### Development ###
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

2. (i3) - this should be taken care of by the copied config files.

Other Manual Configuration
--------------------------

For "development" machines:

1. It may be necessary to manually set the terminal transparency.  Right click
   in the terminal window, choose "Preferences", and set the opacity as desired.
