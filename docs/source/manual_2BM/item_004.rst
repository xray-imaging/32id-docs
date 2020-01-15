Data reconstruction
===================

At the APS
----------

Your raw data are automatically copied from the detector to the analysis computer (handyn in this example) under the folder /local/data/YYYY-MM/PI_lastName. After the transfer the data are also automatically reconstructed with:: 

    [tomo@handyn,~]$ tomopy recon --reconstruction-type try --hdf-file /local/data.h5


Login at the beamline Linux machine handyn as user “tomo” then type::

    [tomo@handyn,~]$ tomopy recon -h


for help. More detailed instruction are at https://github.com/tomography/tomopy-cli

To do a test reconstruction just type::

    [tomo@handyn,~]$ tomopy recon --hdf-file /local/data/YYYY-MM/PI_lastName/file.h5 


At your home institution
------------------------

Install the following::

    Conda: https://www.anaconda.com/download/
    tomopy: conda install -c conda-forge tomopy
    tomopy-cli: https://github.com/tomography/tomopy-cli

then you can run reconstrutions with::

    $ tomopy recon --hdf-file /data/file.h5

or find the rotation axis for all datasets in /data with::

    $ tomopy find_center --hdf-file /data/
