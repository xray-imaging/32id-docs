Energy 
======

`energy <https://github.com/decarlof/tomo2bm/blob/master/flir/energy>`_ is a python script that changes the 2-BM beamline energy configuration. 

Usage
-----

Login into user2bmb@arcturus then::

    bash
    cd ~/2bm-ops/
    energy mono 24.9
    energy pink 2.657
    energy white

for help::

    energy -h

Testing mode
------------

In testing mode, the motor positions are printed but not actual motor motion occurs. To enable testing mode set:: 

    TESTING = True 

in `energy_lib <https://github.com/decarlof/tomo2bm/blob/master/flir/libs/energy_lib.py>`_