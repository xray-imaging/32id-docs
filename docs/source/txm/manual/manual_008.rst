Data Tagging
============

To tag the datasets collected during the experiment with user information we use `DMagic <https://dmagic.readthedocs.io/en/latest/>`_.

DMagic automatically retrieved the current user information from the `Advanced Photon Source <http://www.aps.anl.gov>`_
`scheduling system  <https://schedule.aps.anl.gov/>`_.


To use DMagic during an experiment::

	[usertxm@txmtwo]$ bash
	[usertxm@txmtwo]$ conda activate dm
	[usertxm@txmtwo]$ source /home/dm_id/etc/dm.setup.sh
	[usertxm@txmtwo]$ dmagic -h
	[usertxm@txmtwo]$ dmagic show

if required set the beamline name and tomoScan prefix with::

	[usertxm@txmtwo]$ dmagic show --beamline 32-ID --tomoscan-prefix 32id:TomoScan

::

	2021-07-08 13:00:55,946 - Today's date: 2021-07-08 13:00:55.946907
	2021-07-08 13:00:56,525 - Added fenter@anl.gov to the e-mail list.
	2021-07-08 13:00:56,526 - Added sturchio@udel.edu to the e-mail list.
	2021-07-08 13:00:56,526 - Added sslee@anl.gov to the e-mail list.
	2021-07-08 13:00:56,526 - Added ialmazn@anl.gov to the e-mail list.
	2021-07-08 13:00:56,526 - Added bektur@udel.edu to the e-mail list.
	2021-07-08 13:00:56,526 - Added youngjkm@anl.gov to the e-mail list.
	2021-07-08 13:00:56,596 - 	Run Name: 2021-2
	2021-07-08 13:00:56,596 - 	Proposal Title: Replacement of calcium carbonate (CaCO3) polymorphs by lead, zinc, and cadmium carbonates
	2021-07-08 13:00:56,596 - 	PI Name: Youngjae Kim
	2021-07-08 13:00:56,596 - 	Start time: 2021-07-08 08:00:00-05:00
	2021-07-08 13:00:56,597 - 	End Time: 2021-07-11 08:00:00-05:00
	2021-07-08 13:00:56,597 - 	User email address: 
	2021-07-08 13:00:56,597 - 		fenter@anl.gov
	2021-07-08 13:00:56,597 - 		sturchio@udel.edu
	2021-07-08 13:00:56,597 - 		sslee@anl.gov
	2021-07-08 13:00:56,597 - 		ialmazn@anl.gov
	2021-07-08 13:00:56,597 - 		bektur@udel.edu
	2021-07-08 13:00:56,598 - 		youngjkm@anl.gov
	2021-07-08 13:00:56,598 - General
	2021-07-08 13:00:56,598 -   config           /home/beams/USERTXM/dmagic.conf
	2021-07-08 13:00:56,598 -   verbose          True
	2021-07-08 13:00:56,598 - Settings
	2021-07-08 13:00:56,598 -   beamline         32-ID
	2021-07-08 13:00:56,598 -   tomoscan_prefix  32id:TomoScan

To automatically fill the tomoScan current user info::

	[usertxm@txmtwo]$ dmagic tag
