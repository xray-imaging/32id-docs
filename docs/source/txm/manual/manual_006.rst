Detector
========

The detection system consists of camera, lens and scintillator screens. Below we list of the camera in use at 32-ID:

.. _flir_web_site:  https://www.flir.com/products/blackfly-s-gige/?model=BFS-PGE-161S7M-C
.. _camera_order_00001: https://apps.inside.anl.gov/paris/req.jsp?reqNbr=G1-209025
.. _camera_specs: https://anl.box.com/s/wv9vy7bfle01gvxtxy5g6esght33ixpe

+---------------------------+--------------------+--------------+------------------+---------+------------+--------------------+-----------------------------------------+-------------------------------+
|        Camera             |       Web Site     | pixels (HxV) | pixels size (μm) |   bit   | fps        |      Manual        | Part number                             |          Purchase orider      |
+===========================+====================+==============+==================+=========+============+====================+=========================================+===============================+
| Blackfly S GigE           |  flir_web_site_    | 5230 x 3032  |       2.74       | 8-10-12 | 7          |    camera_specs_   | BFS-PGE-161S7M-C                        |   camera_order_00001_         |
+---------------------------+--------------------+--------------+------------------+---------+------------+--------------------+-----------------------------------------+-------------------------------+


The computers supporting the Blackfly S GigE detector is:

+-----------+--------------+-------------------+-----------------+--------------------------+---------------------+
| Station   | Name         |      Model        |  Product No.    |    Serial No.            |        Manual       |
+-----------+--------------+-------------------+-----------------+--------------------------+---------------------+
| 32-ID-C   | txmtwo       | HP Z820           |                 |                          |                     |
+-----------+--------------+-------------------+-----------------+--------------------------+---------------------+


To start/stop/check the detector epics IOC::

   [usertxm@txmtwo]$ 32idARV2 start
   [usertxm@txmtwo]$ 32idARV2 stop
   [usertxm@txmtwo]$ 32idARV2 status


the detector user interface is accessible with::

   [usertxm@txmtwo]$ 32idARV2 medm

or by selecting **detector** from the main TXM medm screen.

Note: old version of AreaDetector for the TXM camera is accassible using **32idARV1** alias.


Power cycle
-----------

To power cycle the Blackfly you can use the power management unit (PDI) **s32pdu1** outlet #1


32-ID screens
-------------

.. image:: ../img/ADAravis_32-ID_screen0.png
   :width: 320px
   :align: center
   :alt: 

.. image:: ../img/ADAravis_32-ID_screen1.png
   :width: 320px
   :align: center
   :alt: 

.. image:: ../img/ADAravis_32-ID_screen2.png
   :width: 320px
   :align: center
   :alt: 


13-BM screens
-------------

.. image:: ../img/ADAravis_13-BM_screen1.png
   :width: 320px
   :align: center
   :alt: 

.. image:: ../img/ADAravis_13-BM_screen2.png
   :width: 320px
   :align: center
   :alt: 


