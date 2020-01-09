Tomo@0deg and Tomo@90deg
========================

.. contents:: 
   :local:


The Tomo@0deg and Tomo@90deg motors are not responding (control screes is white)


These two motors are controlled by an EPICS softIOC. If the screen for Tomo@0deg and Tomo@90deg
are white it means that the softIOC was not started. To solve this please run::

    [user2bmb@arcturus]$ start_2bmS1.sh


or you can directly stop/start with::

    [user2bmb@arcturus]$ cd /net/s2dserv/xorApps/epics/synApps_5_8/ioc/2bmS1/iocBoot/ioc2bmS1Linux/
    [user2bmb@arcturus]$ ./2bmS1.sh start
    [user2bmb@arcturus]$ ./2bmS1.sh stop

