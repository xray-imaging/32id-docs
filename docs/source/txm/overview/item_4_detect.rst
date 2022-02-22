Detection - resolution - FOV
============================

Detection system
----------------
The X-ray detection system consists of camera, lens and scintillator screens. The pixel size and the resolving power of the detection system is not the most relevant information for a TXM since the final resolution and field of view (FOV) depends on the magnification obtained with the Fresnel zone plate objective lens performed in the X-ray regim.

.. _camera_00003:  https://www.ptgrey.com/grasshopper3-50-mp-mono-usb3-vision-sony-pregius-imx250
.. _camera_00004:  https://www.flir.com/products/blackfly-s-gige/?model=BFS-PGE-161S7M-C
.. _manual:  https://anl.box.com/s/m8qlbi1dr3jn1l8fwbraar0wvy2y94bk
.. _manual2:  https://www.flir.com/support-center/iis/machine-vision/knowledge-base/technical-documentation-bfs-gige/

+-------------------------------------------------------------+--------------+------------------+---------+------------+-------------------+--------------------+--------------------+
|                   Camera                                    | pixels (HxV) | pixels size (μm) |   bit   | fps        | manual            |      FLIR Web doc  | Part number        |
+=============================================================+==============+==================+=========+============+===================+====================+====================+
| Blackfly S GigE BFS-PGE-161S7M-C: 16.1 MP,  Sony IMX542.    | 5320 x 3032  |       2.74       | 8,10,12 | 7          | manual2_          |     camera_00004_  | GS3-U3-51S5M-C     |
+-------------------------------------------------------------+--------------+------------------+---------+------------+-------------------+--------------------+--------------------+


Full technical specification are in manual2_.


| This camera is coupled with a Thorlabs 83 mm tube lense and a `5X Mitutoyo Plan Infinity Corrected Objective <https://www.edmundoptics.com/p/5x-mitutoyo-plan-apo-infinity-corrected-long-wd-objective/6621>`_, or `10X Mitutoyo Plan Infinity Corrected Objective <https://www.edmundoptics.com/p/10x-mitutoyo-plan-apo-infinity-corrected-long-wd-objective/6623/>`_ .

Resolution & FOV
~~~~~~~~~~~~~~~~

| The table below shows the FOV and spatial resolution obtained with the TXM for different X-ray energies, FZPs and [sample to detector] distances.

.. image:: ../img/TXM_calc.jpg
   :width: 800px
   :align: center
   :alt: project


