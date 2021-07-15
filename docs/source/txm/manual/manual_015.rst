User Interface 
==============

TXM Optics
----------

Open a terminal::

    $ bash
    $ cd ~/TXM_UI/
    $ ./tomography.sh

The following window will open:

.. image:: img_guide/GUI_main_window.png
   :width: 1200px
   :align: center
   :alt: project

Now, to open the window controlling the stages, go in <View> <Beamline calibration> menu
This new window will open:

.. image:: img_guide/GUI_main_control_window.png
   :width: 1200px
   :align: center
   :alt: project

To load a scan script like "tomo_step_scan.py" or "tomo_fly_scan.py", click on the “+” button on the lower right corner of the main window.

Scan scripts are in this location::

    $ cd /home/beams/USR32IDC/TXM_control/pg/


**Note:** scanning scripts can be run directly from python::
    
    $ /local/usr32idc/Anaconda/bin/python tomo_fly_scan.py

or directly from spyder.


EPICS screens 
-------------

To open the EPICS screens, one needs first to start **caQtDM**.

Open a terminal and type::

    $ start_caQtDM_32id

The window "32id_beamline.ui" will open. 

.. image:: img_guide/medm_main_window.png
   :width: 1200px
   :align: center
   :alt: project

| **More control**
| To open the window offering more control options, click on "Admin".
| From there, it is possible to restart ImageJ or the interface for the control of the camera by pushing the button shown in the screenshot.

.. image:: img_guide/medm_stages.jpg
   :width: 1000px
   :align: center
   :alt: project

**Air pressure for the sample stage**

| 1) In the window entitled “"32id_beamline.ui", click on the brown button “IOC’s”
| 2) click on the brown button “32idcPLC”
| 3) click on “Digital”
| 4) click on “Granite Air Valves (caQtDM-only)”

.. image:: img_guide/medm_PLC_granite.jpg
   :width: 1000px
   :align: center
   :alt: project

.. image:: img_guide/granite_air_valves.jpg
   :width: 600px
   :align: center
   :alt: project
