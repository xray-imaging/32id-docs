EPICS ioc reboot
================ 

.. contents:: 
   :local:

To reboot the 2bma or 2bmb ioc::

    [user2bmb@arcturus]$ iocConsole ioc2bma
    [user2bmb@arcturus]$ reboot

or::

    [user2bmb@arcturus]$ iocConsole ioc2bmb
    [user2bmb@arcturus]$ reboot

Before rebooting an IOC you can verify that the autosave files are up to date with::

    [user2bmb@arcturus]$ /APSshare/epics/synApps_5_8/support/autosave-5-7-1/bin/linux-x86_64/asVerify auto_positions.sav
    [user2bmb@arcturus]$ /APSshare/epics/synApps_5_8/support/autosave-5-7-1/bin/linux-x86_64/asVerify auto_settings.sav
