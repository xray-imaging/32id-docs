Globus & Data Formats
=====================

All internal data transfer is handled by `Globus <https://www.globus.org>`_, if the beamline globus server is down make sure to
start the local `Globus EndPoint <https://www.globus.org/globus-connect-personal>`_ with:


Log in as usertxm@txmtwo::

	[usertxm@txmtwo]$ cd /local/Software/globusconnectpersonal-3.2.5/
	[usertxm@txmtwo]$ globusconnect
	
To open the data transfer GUI, log in as usertxm@txmthree::

	[usertxm@txmthree]$ source /home/dm_id/etc/dm.setup.sh
	[usertxm@txmthree]$ dm-station-gui


To use a specific key::

	txmthree: nohup ./globusconnectpersonal -restrict-paths /local/ssd/data -dir $HOME/.globusonline_txmthree -shared-paths /local/ssd/data -start &
	txmtwo: nohup ./globusconnectpersonal -restrict-paths /local/dataraid -dir $HOME/.globusonline_txmtwo -shared-paths /local/dataraid -start &


**Data Formats**

+-----------------------------------------------+-------------------------------------+
|                        Data Format            |           Visualization Tool        |
+===============================================+=====================================+
|                        TIFF                   |           ImageJ                    |
+-----------------------------------------------+-------------------------------------+
|                        HDF5                   |           ImageJ                    |
+-----------------------------------------------+-------------------------------------+
|                        ZARR                   |           ImageJ                    |
+-----------------------------------------------+-------------------------------------+












