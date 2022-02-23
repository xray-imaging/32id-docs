Data Analysis
=============

.. _cluster_folder: https://anl.box.com/s/cwqbvet2qv8239nhrof0qemyohd0jho3
.. _cluster: https://anl.box.com/s/uysvb5ujnlugmd16r2f6o10fem9rjgvr
.. _disk_array: https://anl.box.com/s/zzyvv7w80ltwbtf09zrjiqiw7ak6i7ge
.. _cluster_quote: https://anl.box.com/s/j7wz6li4afoq2gs5g8feehmmz8q7whuy
.. _disk_array_quote: https://anl.box.com/s/sbft8cbt2xcpzuuvikixr82dn9jf6zog

For tomographic reconstruction 32-ID TXM is typically done on machine txmthree: Intel Xeon i7 Silver 4214, 192GB RAM, NVidia Quadro RTX 4000 (8GB), 1TB SSD. 
For processing huge data volumes the instrument relies on the micro tomography computing infrastructure located at 2-BM:

+-----------+--------------+---------------+-----------------+---------------------------------+----------------------+
| Station   | Name         | Product       | Part list       |      Model                      |      Quote           |
+-----------+--------------+---------------+-----------------+---------------------------------+----------------------+
| 2-BM      | tomo 1-2     | MNJ15421064   | `cluster`_      |  Supermicro 740GP-TNRT cluster  | `cluster_quote`_     |
+-----------+--------------+---------------+-----------------+---------------------------------+----------------------+
| 2-BM      | disk array   | MNJ15508749   | `disk_array`_   |  SYS-220U-TNR Storage           | `disk_array_quote`_  |
+-----------+--------------+---------------+-----------------+---------------------------------+----------------------+


At the APS
----------

Your raw data are automatically copied from the detector to the analysis computer (txmthree in this example) under the folder /local/ssd/data/YYYY-MM/PI_lastName. 
The SSD storage is limited, therefore after processing it is recommended to move data to a slower but larger HDD storage /local/data/YYYY-MM/PI_lastName. 

Manual
~~~~~~

To manually reconstruct a data set, use the `tomopy cli tool <https://github.com/tomography/tomopy-cli>`_. 
::

    [usertxm@txmthree,~]$ bash
    [usertxm@txmthree,~]$ conda activate tomopy

then for help::

    [usertxm@txmthree,~]$ tomopy recon -h

To do a test reconstruction type::

    [usertxm@txmthree,~]$ tomopy recon --file-name /local/data/YYYY-MM/PI_lastName/file.h5 

Automatic
~~~~~~~~~

To setup a reconstruction to start automatically type::

    [usertxm@txmthree,~]$ bash
    [usertxm@txmthree,~]$ auto_rec /local/data/YYYY-MM/PI_lastName/

auto_rec runs tomopy recon for each newly transferred data set with the following options::

    tomopy recon --reconstruction-type try --file-name /local/data/YYYY-MM/PI_lastName/data.h5


At your home institution
------------------------

Install the following:

1. Download and install `anaconda python <https://www.anaconda.com/download/>`_ for your operative system.
2. Create a conda environment:
    
::

    $ conda create -n tomopy python=3.9

3. Activate the newly created conda environment:

::

    $ conda activate tomopy


4. Install `tomopy <https://tomopy.readthedocs.io/en/latest/>`_:

::

    $ conda install --channel conda-forge tomopy


5. Install `dxchange <https://dxchange.readthedocs.io/en/latest/>`_:

::

    $ conda install -c conda-forge dxchange

6. Install `tomopy cli <https://tomopycli.readthedocs.io/en/latest/>`_:

::

    $ git clone https://github.com/tomography/tomopy-cli.git
    $ cd tomopy-cli
    $ python setup.py install

7. Install `tomopy cli dependecy <https://github.com/tomography/tomopy-cli/blob/master/requirements.txt>`_:

::

    pip install opencv-python


To run a reconstuction you can now run::

    $ tomopy recon --file-name /data/file.h5


Step-by-step installation on a Windows machine
----------------------------------------------

See video https://anl.app.box.com/file/834443962638?s=182dsmpnxx25o2xsy6n1ozgj8rx5omjg


Reconstruction on GPU
---------------------
If your machine is equipped with an NVidia GPU such as the one installed in txmthree or tomo1/tomo2, then reconstruction can be done with the `tomocupy cli tool <https://github.com/tomography/tomocupy-cli>`_. The syntax is the same as in tomopy-cli.
::

    $ tomocupy -h


