Post-install Tasks - Common
===========================

The following tasks should be performed after a new machine is provisioned 
using Ansible.  This consists mainly of installing AUR pakcages and configuring 
them.  The AUR is not well suited to automation; many packages require manual 
intervention.  It is for this reason that (for now), installation of software
from the AUR must be performed manually.

Install AUR Packages
--------------------

* cower
* pacaur
* google-chrome
* vim-pathogen
* numix-themes-blue
* numix-themes-darkblue
* numix-themes-electric
* numix-frost-themes
* numix-icon-theme-git
* numix-bevel-icon-theme-git
* numix-shine-icon.theme-git

Other Manual Configuration
--------------------------

1. Edit cower's config file as `~/.config/cower/config`.  Add the line 

		TargetDir=$HOME/AUR

Window Manager Configuraton (Openbox) 
-------------------------------------

This section is for "general" machines.

1. Run `lxappearance` and set the following configurations:

	* Widget theme: Numix Frost
	* Font: Source Sans Pro 10
	* Icon theme: Numix

2. (Openbox) - run `obconf` and set the following configurations:

	* Theme: Numix Frost

Window Manager Configuration (i3)
---------------------------------

This section is for "development" machines.

TODO