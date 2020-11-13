Rebooting the CCD
=================

Open a terminal

First, check the status typing::

    $ 32idcPG1 status

If the IOC is running, the message would be::

    $ /xorApps/epics/AD-3-3-2/ioc/ADPointGrey/iocs/pointGreyIOC/bin/linux-x86_64/pointGreyApp st.cmd
    $ 32idcPG1 is running

Then, stop the IOC::

    $ 32idcPG1 stop

Restart the IOC::

    $ 32idcPG1 start

