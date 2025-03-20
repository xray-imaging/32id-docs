Data Tagging
============

To tag the datasets collected during the experiment with user information we use `DMagic <https://dmagic.readthedocs.io/en/latest/>`_.

DMagic automatically retrieved the current user information from the `Advanced Photon Source <http://www.aps.anl.gov>`_
`scheduling system  <https://schedule.aps.anl.gov/>`_.

(dm) usertxm@txm4
To use DMagic during an experiment::

	usertxm@txm4 $ bash
	(base) usertxm@txm4 $ conda activate dm
	(dm) usertxm@txm4 $ 
	(dm) usertxm@txm4 $ dmagic -h
	(dm) usertxm@txm4 $ dmagic show

if required set the beamline name and tomoScan prefix with::

	usertxm@txm4 $ dmagic show --beamline 32-ID-B,C --tomoscan-prefix 32id:TomoScan

::

	2025-03-20 15:48:05,583 - Today's date: 2020-11-01 15:48:05.583378-06:00
	2025-03-20 15:48:19,304 - Found valid proposal start time
	2025-03-20 15:48:19,305 - 	Run: 2020-3
	2025-03-20 15:48:19,305 - 	PI Name: Kamel Fezzaa
	2025-03-20 15:48:19,305 - 	PI affiliation: Argonne National Laboratory
	2025-03-20 15:48:19,305 - 	PI e-mail: fezzaa@aps.anl.gov
	2025-03-20 15:48:19,305 - 	PI badge: 51803
	2025-03-20 15:48:19,305 - 	Proposal GUP: 71795
	2025-03-20 15:48:19,305 - 	Proposal Title: 32-ID operation and RnD for 2020-3
	2025-03-20 15:48:19,305 - 	Start date: 2020_10_20
	2025-03-20 15:48:19,305 - 	Start time: 2020-10-20 08:00:00-05:00
	2025-03-20 15:48:19,305 - 	End Time: 2020-11-09 08:00:00-06:00
	2025-03-20 15:48:19,305 - 	User email address: 
	2025-03-20 15:48:19,305 - 		 vdeandrade@aps.anl.gov
	2025-03-20 15:48:19,305 - 		 fezzaa@aps.anl.gov
	2025-03-20 15:48:19,305 - 		 deriy@anl.gov
	2025-03-20 15:48:19,305 - General
	2025-03-20 15:48:19,305 -   config           /home/beams/USERTXM/dmagic.conf
	2025-03-20 15:48:19,305 -   verbose          True
	2025-03-20 15:48:19,305 - Settings
	2025-03-20 15:48:19,305 -   beamline         32-ID-B,C
	2025-03-20 15:48:19,305 -   credentials      /home/beams/USERTXM/.scheduling_credentials
	2025-03-20 15:48:19,305 -   set              0
	2025-03-20 15:48:19,305 -   tomoscan_prefix  32id:TomoScanStep:
	2025-03-20 15:48:19,305 -   url              https://beam-api-dev.aps.anl.gov

To automatically fill the tomoScan current user info::

	usertxm@txm4 $ dmagic tag
