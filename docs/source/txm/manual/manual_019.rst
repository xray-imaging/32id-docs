Energy scan 
================

Create a list of energies as .npy file::

	(tomoscan) usertxm@txmtwo ~ $ python
	Python 3.9.7 (default, Sep 16 2021, 13:09:58) 
	[GCC 7.5.0] :: Anaconda, Inc. on linux
	Type "help", "copyright", "credits" or "license" for more information.
	>>> import numpy as np
	>>> energies = np.linspace(8.3,8.5,10)
	>>> energies
	array([8.3       , 8.32222222, 8.34444444, 8.36666667, 8.38888889,
       	       8.41111111, 8.43333333, 8.45555556, 8.47777778, 8.5       ])
	>>> np.save('energies/energies.npy',energies)

	

