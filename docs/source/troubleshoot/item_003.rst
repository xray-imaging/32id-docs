FLIR fails to boot
==================

.. contents:: 
   :local:

If the area detector IOC controlling the FLIR camare fails to boot with even after a camera power cycle, it means that the last auto save file (auto_setting.sav) is corrupted. To recover you need to replace the corrupted auto save with a good one::


    user2bmb@pg10ge$ cd ~/iocSpinnaker/autosave/
    user2bmb@pg10ge$ cp auto_settings.sav_good auto_settings.sav

then restart areadetector with::

    ~/2bmbOryx.sh start
