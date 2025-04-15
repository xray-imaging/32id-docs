Beamline Control
================

All beamline components and detectors are controlled using `EPICS <https://epics-controls.org/>`_ and `areaDetector <https://areadetector.github.io/master/index.html>`_.
Each device can be configure and controlled through a graphic user interface (GUI) or through a python script using `PyEpics <https://cars9.uchicago.edu/software/python/pyepics3/>`_.

Main interface
--------------

To start the main TXM control user interface with txmOptics, tomoScan IOCs and associated python servers ::

    [usertxm@txm4]$ start_txm.sh


.. image:: img_guide/txm_main.png
   :width: 1000px
   :align: center
   :alt: project
   
To start the 32-ID beamline control for users (limited functionality, no IOC restart)::

    [usertxm@txm4]$ start_txm_gui.sh

.. image:: img_guide/txm_main_user.png
   :width: 1000px
   :align: center
   :alt: project


Other EPICS IOCs
----------------

The TXM instrument relies on several hardware components, all supported by EPICS. If you see any white field in the main TXM control user 
interface, it means the associated EPICS IOC is not running. To start/stop/check the status of each IOC use the table below to ssh in the 
corresponding server and run the corresponding command using the following::

   [username@server] $ IOC-name status
   [username@server] $ IOC-name start
   [username@server] $ IOC-name stop


+---------------+------------------------+-------------------------------------------------------------------------------------------------+
|    IOC-Name   |       server           |                                                 Description                                     |
+===============+========================+=================================================================================================+
|  32idaSoft    |   usr32idc@txm4        | Runs white beam slits, Queensgate (pitch and roll monochromator)                                |
+---------------+------------------------+-------------------------------------------------------------------------------------------------+
|  32idbSoft    |   usr32idc@txm4        | OMS MXA Motors: Detector(X,Y),Tube(Z),CCD(Y),Condenser(Z),Sample(Y, granite), TXM(granite),     |
|               |                        | TXM Transport, PLC (Granite air valves)                                                         |
+---------------+------------------------+-------------------------------------------------------------------------------------------------+
|  32idbTXM     |   usr32idc@txm4        | SmarAct Stages: Zone Plates(X,Y,Z), Sample Top (X,Z), Condenser(X,Y,Pitch,YAW),                 |
|               |                        | Scintillator(Pitch,YAW,Focus), Beamstop(X,Y), PinHole(X,Y), Diffuser(X), BPM(X,Y), Aerotech     |
|               |                        | NewFocus Piezo: CCD Rotation, Sample(X, granite), Uniblitz Shutter, Analox He Sensor            |
+---------------+------------------------+-------------------------------------------------------------------------------------------------+
|  32idbBPM     |   usr32idc@txm4        | SYDOR BPM                                                                                       |
+---------------+------------------------+-------------------------------------------------------------------------------------------------+
|  32idbShaker  |   usr32idc@32idbws2    | Condenser shaker (windows)                                                                      |
+---------------+------------------------+-------------------------------------------------------------------------------------------------+
|  32idbSP1     |   usertxm@gauss        | FLIR Oryx server                                                                                |
+---------------+------------------------+-------------------------------------------------------------------------------------------------+
|  32kinetix    |   usertxm@maxwell      | TELEDYNE Kinetix server                                                                         |
+---------------+------------------------+-------------------------------------------------------------------------------------------------+



32-ID beamline control
----------------------

For opening the main 32-ID beamline control user interface (caQTdm), select **32-ID Beamline** in the top left part of the main TXM gui.

.. image:: img_guide/medm_main_window.png
   :width: 700px
   :align: center
   :alt: project


Tomography
----------

For tomographic data acqusition, select **TomoScan** in the top left part of the main txm gui. `TomoScan <https://tomoscan.readthedocs.io/en/latest/>`_ is a general interface for tomographic scanning in use at seveal beamlines at the APS (2-BM, 7-BM, 13-BM, and 32-ID):

.. image:: img_guide/tomoScan.png
   :width: 400px
   :align: center
   :alt: project