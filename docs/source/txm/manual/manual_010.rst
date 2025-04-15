Detection CMOS Cameras
======================

The detection system consists of camera, lens and scintillator screens. Below we list of the camera in use at 32-ID:

.. _flir_web_site:  https://www.flir.com/products/blackfly-s-gige/?model=BFS-PGE-161S7M-C
.. _camera_order_00001: https://apps.inside.anl.gov/paris/req.jsp?reqNbr=G1-209025
.. _camera_specs: https://anl.box.com/s/wv9vy7bfle01gvxtxy5g6esght33ixpe
.. _camera_order_00002: https://apps.inside.anl.gov/paris/req.jsp?reqNbr=G3-353064
.. _camera_specs2: https://anl.app.box.com/file/710576385443?s=7pe793z5x9cspayqimscavzqhdcc9og7
.. _camera_order_00003: https://apps.inside.anl.gov/paris/req.jsp?reqNbr=G3-087053
.. _camera_specs3: https://www.teledynevisionsolutions.com/products/kinetix/?model=01-KINETIX-M-C&vertical=tvs-photometrics&segment=tvs





+---------------------------+--------------------+--------------+------------------+---------+-------+--------------------+---------------------+----------------------+----------------------+
|        Camera             |       Web Site     | pixels (HxV) | pixels size (μm) |   bit   | fps   |      Manual        | Part number         |  Purchase order      |  Server              |
+===========================+====================+==============+==================+=========+=======+====================+=====================+======================+======================+
| Blackfly S GigE           |  flir_web_site_    | 5230 x 3032  |       2.74       | 8-10-12 | 7     |    camera_specs_   | BFS-PGE-161S7M-C    | camera_order_00001_  |  gauss               |
+---------------------------+--------------------+--------------+------------------+---------+-------+--------------------+---------------------+----------------------+----------------------+
| Teledyne Oryx             |  flir_web_site_    | 6464 x 4852  |       3.45       | 8-10-12 | 26    |    camera_specs2_  | Oryx 10GigE: 31 MP  | camera_order_00002_  |  gauss               |
+---------------------------+--------------------+--------------+------------------+---------+-------+--------------------+---------------------+----------------------+----------------------+
| Teledyne Kinetix          |  flir_web_site_    | 3200 x 3200  |       6.5        | 8-10-12 | 500   |    camera_specs3_  | Kinetix             | camera_order_00003_  |  maxwell             |
+---------------------------+--------------------+--------------+------------------+---------+-------+--------------------+---------------------+----------------------+----------------------+


To start/stop/check the detector (ORYX) epics IOC - mind to use the correct server::

   [usertxm@gauss]$ 32idbSP1 start
   [usertxm@gauss]$ 32idbSP1 stop
   [usertxm@gauss]$ 32idbSP1 status


the detector user interface is accessible with::

   [usertxm@gauss]$ 32idbSP1 medm

To start/stop/check the detector (KINETIX) epics IOC::

   [usertxm@maxwell]$ 32kinetix start
   [usertxm@maxwell]$ 32kinetix stop
   [usertxm@maxwell]$ 32kinetix status


the detector user interface is accessible with::

   [usertxm@maxwell]$ 32kinetix medm


or by selecting **detector** from the main TXM medm screen.

Note: old version of AreaDetector for the TXM camera is accessible using **32idARV1** alias.


Power cycle
-----------

To power cycle the Blackfly you can use the power management unit (PDI) **s32pdu1** outlet #1





