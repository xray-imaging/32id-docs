32-ID Docs
==========


`32-ID Docs <https://docs32id.readthedocs.io>`_ provides instruction and troubleshoting information to operate the APS beamline 32-ID


Features
--------

* Documentation: https://docs32id.readthedocs.io
* Issue Tracker: https://github.com/xray-imaging/32id-docs/issues

To edit/modify these web pages
------------------------------

- install `Anaconda python <https://www.anaconda.com/products/individual>`_ if you already have it installed open a terminal and update with:

::
    
    conda update all

once installed add the following packages in a teminal::

    conda install sphinx
    conda install sphinxcontrib
    pip install sphinx-rtd-theme
    pip install pybtex
    pip install sphinxcontrib-bibtex

If you need a text editor install:
https://www.sublimetext.com/3

- create a github account https://github.com/

- make sure git is installed on your computer by opening a terminal and typing::

    git

If git is not installed:
    git for mac: 
        select command line tools from 
        https://developer.apple.com/download/more/
    or
        https://git-scm.com/download/mac

- go to https://github.com/xray-imaging/32id-docs and fork the repository
- Press the green "Code" button and copy the repository http address. This is in the format of
https://github.com/GITUSER/32id-docs.git where GITUSER is your git user name, then::

    git clone https://github.com/GITUSER/32id-docs.git
    cd 32id-docs/docs
    make clean
    make html

then open a web browser and in the address type: file:///.../32id-docs/docs/_built/html/index.html
where ... is the path to the 32id-docs


