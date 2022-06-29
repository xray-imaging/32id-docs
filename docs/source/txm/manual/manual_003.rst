Data Analysis
=============

.. _cluster_folder: https://anl.box.com/s/cwqbvet2qv8239nhrof0qemyohd0jho3
.. _cluster: https://anl.box.com/s/uysvb5ujnlugmd16r2f6o10fem9rjgvr
.. _disk_array: https://anl.box.com/s/zzyvv7w80ltwbtf09zrjiqiw7ak6i7ge
.. _cluster_quote: https://anl.box.com/s/j7wz6li4afoq2gs5g8feehmmz8q7whuy
.. _disk_array_quote: https://anl.box.com/s/sbft8cbt2xcpzuuvikixr82dn9jf6zog

Tomographic reconstruction of 32-ID TXM data is typically done on machine txmthree.xray.aps.anl.gov: Intel Xeon i7 Silver 4214, 192GB RAM, NVidia Quadro RTX 4000 (8GB), 4TB SSD. 
For processing huge data volumes the instrument relies on the micro tomography computing infrastructure located at 2-BM:

+-----------+--------------+---------------+-----------------+---------------------------------+----------------------+
| Station   | Name         | Product       | Part list       |      Model                      |      Quote           |
+-----------+--------------+---------------+-----------------+---------------------------------+----------------------+
| 2-BM      | tomo 1-2     | MNJ15421064   | `cluster`_      |  Supermicro 740GP-TNRT cluster  | `cluster_quote`_     |
+-----------+--------------+---------------+-----------------+---------------------------------+----------------------+
| 2-BM      | disk array   | MNJ15508749   | `disk_array`_   |  SYS-220U-TNR Storage           | `disk_array_quote`_  |
+-----------+--------------+---------------+-----------------+---------------------------------+----------------------+



Reconstruction on CPU and GPU at the APS
----------------------------------------

Your raw data are automatically copied from the detector to the analysis computer (txmthree in this example) under the folder /local/ssd/data/YYYY-MM/PI_lastName. 
The SSD storage is limited, therefore after processing it is recommended to move data to a slower but larger HDD storage /local/data/YYYY-MM/PI_lastName. 


Open tabs  for reconstruction of 1 slice, full volume, google slides logging, Fiji, and data folder with reconstrutions. 

::

    [usertxm@txmthree,~]$ ~/start_rec.sh
    
The tabs will have appropriate conda environment activated and show examples of running reconstructions. 
.. image:: img_guide/rec_tabs.png
   :width: 400px
   :align: center
   :alt: project

.. image:: img_guide/rec_tabs1.png
   :width: 400px
   :align: center
   :alt: project
   


Reconstruction on CPU and GPU at your home institution
------------------------------------------------------
Download and install either `tomocupy cli tool <https://github.com/tomography/tomocupy-cli>`_ (reconstruction on GPU) or `tomopy cli tool <https://github.com/tomography/tomopy-cli>`_ (reconstruction on CPU). Syntax is similar for both packages. List of commands:
::

    $ tomocupy -h


