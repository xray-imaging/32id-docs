Linux Workstation
=================

Mouse
-----

If you need to make the mouse larger on a RedHat linux machine::

    $ gsettings set org.gnome.desktop.interface cursor-size 48

Workspace
---------

To change to 5 worskpaces::

	$ /usr/bin/gsettings set org.gnome.desktop.wm.preferences num-workspaces "5"


To change their names::

	$ /usr/bin/gsettings set org.gnome.desktop.wm.preferences workspace-names "['Com', 'Vienna', 'Test1', 'Test2','Test3']"

Reboot
------

Currently these machine/username have permission to reboot from the terminal::

	usr32idc@txmone $ sudo /usr/sbin/reboot
	usr32idc@txmtwo $ sudo /usr/sbin/reboot

