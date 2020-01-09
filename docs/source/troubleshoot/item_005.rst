GUI play/stop are disabled
==========================

.. contents:: 
   :local:

If after loading a scan script in Tomo GUI (started with ~/MCT/tomography.sh) the play and stop buttons are disabled press the camera acquire/stop. If it stays disabled is because the camera that was run last time is off and the GUI thinks the camera to be still collecting images.   
To solve the situation, go to::

    [user2bmb@arcturus,43,~]$ cd .config/UChicagoArgonneLLC/
    [user2bmb@arcturus,44,UChicagoArgonneLLC]$ ls
    [user2bmb@arcturus,44,UChicagoArgonneLLC]$ TXM.ini  TXM.ini_good

and edit the TXM.ini to change the camera IOC prefix. Another option is to copy over one of the good ini present in that folder.
