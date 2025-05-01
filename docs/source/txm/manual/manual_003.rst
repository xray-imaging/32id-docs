Data Analysis
=============

At the APS
----------

Your raw data are automatically copied from the detector to the analysis computer (handyn in this example) under the folder /local/data/YYYY-MM/PI_lastName. 

Manual
~~~~~~

To manually reconstruct a data set, use the `tomopy cli tool <https://github.com/tomography/tomopy-cli>`_. 
::

    [tomo@tomo1,~]$ bash
    [tomo@tomo1,~]$ conda activate tomopy

then for help::

    [tomo@tomo1,~]$ tomopy recon -h

To do a test reconstruction type::

    [tomo@tomo1,~]$ tomopy recon --file-name /local/data/YYYY-MM/PI_lastName/file.h5 


Automatic
~~~~~~~~~

To setup a reconstruction to start and publish automatically the results on a google slide with `tomolog <https://tomologcli.readthedocs.io/en/latest/index.html>`_, 
edit tomorec_log

::

    [tomo@tomo1,~]$ bash
    [tomo@tomo1,~]$ conda activate tomocupy
    (tomocupy) [tomo@tomo1,~]$ sublime ~/bin/tomorec_log

by updating the --presentation-url to match the new google slide url

::

    #!/usr/bin/bash
    tomocupy recon --file-name $1 --remove-stripe-method fw --reconstruction-type full --rotation-axis-auto auto --find-center-end-row 1500
    tomolog run --presentation-url https://docs.google.com/presentation/d/1YuxMttfW8w2sfwbaw634R3_LgPIsaHblz4Lrsjzn6ufQ/edit?usp=sharing --file-name $1 --beamline 2-bm --zoom [1,2,4]

then type::

    (tomocupy) [tomo@tomo1,~]$ auto_rec /local/data/YYYY-MM/PI_lastName/

any new raw dataset uploade in /local/data/YYYY-MM/PI_lastName/ will be automatically reconstructed and results will be published on a google slide using `tomolog <https://tomologcli.readthedocs.io/en/latest/index.html>`_.


.. image:: ../img/tomolog_01.png 
   :width: 512px
   :align: center
   :alt: tomo_01



.. _handyn label: https://anl.box.com/s/2kdy0yaz57nfodyv31k4etp83sqckb0x
.. _handyn SM: https://anl.box.com/s/itwhcp9xr7xocl1djilyd5yqf8un6yjt


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

For Windows installation of tomopy-cli watch `this video <https://anl.box.com/s/182dsmpnxx25o2xsy6n1ozgj8rx5omjg>`_.

7. Install `tomopy cli dependecy <https://github.com/tomography/tomopy-cli/blob/master/requirements.txt>`_:

::

    pip install opencv-python


To run a reconstuction you can now run::

    $ tomopy recon --file-name /data/file.h5


Mosaic
------

For samples larger than the field of view we collect multiple data sets consisiting of overlapping tiles to form a mosaic.
To reconstruct these type of data please use `tile <https://tile.readthedocs.io/en/latest/>`_  command-line-interface for mosaic tomography data processing.

