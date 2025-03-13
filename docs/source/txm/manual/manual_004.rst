Data Collection
===============


.. _EPICS_NTNDA_Viewer: https://cars9.uchicago.edu/software/epics/areaDetectorViewers.html
.. _tomoScan: https://tomoscan.readthedocs.io/en/latest/index.html
.. _tomoScanStream: https://tomoscan.readthedocs.io/en/latest/api/tomoscan_stream_2bm.html
.. _tomoStream: https://tomostream.readthedocs.io/en/latest/about.html
.. _PVaccess: https://epics-controls.org/resources-and-support/documents/pvaccess/
.. _Data Exchange: https://dxfile.readthedocs.io/en/latest/source/xraytomo.html

TomoScan
--------

The tomography scans are managed by `tomoScan`_ :cite:`Nikitin2022`. Please refer to the `tomoScan`_ documentation for details.

To configure a single tomographic scan enter the acquistion parameters at:

.. image:: img_guide/tomoScan.png
   :width: 480px
   :align: center
   :alt: tomoScan

Streaming data collection
-------------------------

`tomoScan`_ provides also support for *streaming data collection*:cite:`Nikitin2022` (see `tomoScanStream`_ documentation for details). When collecting data in streaming mode, projections, 
dark and flat images are broadcasted using `PVaccess`_ and can be retrieved as EPICS PVs. 

**Streaming data collection** features are:

#. Projection, dark and flat image broadcast as PV access variables
#. On-demand retake of dark-flat field images
#. On-demand data capturing with saving in a standard `Data Exchange`_ hdf5file
#. Set a number of projectons ("Pre count") collected before a triggered data capturing event to be also saved in the same hdf5 file

All TomoScanStream functionalies can be controlled from the Streaming Control section of:

.. image:: img_guide/tomoScanStream.png
    :width: 70%
    :align: center

Streaming data reconstruction
-----------------------------

The projection, dark and flat image broadcast provided by `tomoScanStream`_ can be used to reconstruct in real-time 3 orthogonal slices. This task is accomplished by `tomoStream`_.

**Streaming data reconstruction** features are:

#. Streaming reconstruction of 3 (X-Y-Z) ortho-slices through the sample

#. On demand adjustment of the

    * X Y Z ortho-slice positions
    * reconstruction rotation center
    * reconstruction filter

All `tomoStream`_ functionalies can be controlled from the tomoStream user interface:

.. image:: img_guide/tomoStream.png
    :width: 60%
    :align: center

The output of **tomostream** is a live reconstruction diplaying in ImageJ using the `EPICS_NTNDA_Viewer`_ plug-in:

.. image:: img_guide/tomoStreamRecon.png
    :width: 70%
    :align: center
    
While the sample is rotating is possible to optimize instrument (alignment, focus, sample to detector distance etc.) and  beamline (energy etc.) conditions and monitor the effect live on the 3 orthogonal slices. It is also possible to automatically trigger data capturing based on events occurring in the sample and its environment as a result of segmentation or machine learning.
