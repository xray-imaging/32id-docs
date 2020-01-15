Auto 
====

`auto <https://github.com/decarlof/2bm-ops/blob/master/auto>`_ is a python script that automates several 2-BM beamline operations tasks. 

Usage
-----

Login into user2bmb@arcturus then::

    bash
    cd ~/2bm-ops
    auto --focus
    auto --res
    auto --axis

for help::

    auto --help
    usage: auto.py [-h] [--res] [--axis] [--roll] [--pitch] [--focus]

    optional arguments:
    -h, --help  show this help message and exit
    --res       measure the image resolution (μm/pixel)
    --axis      find the rotation axis location
    --roll      measure the rotation axis roll
    --pitch     measure the rotation axis pitch
    --focus     focus the scintillator screen
