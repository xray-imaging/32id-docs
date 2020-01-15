Globus
======

`globus <https://github.com/decarlof/globus>`_ is a python script that automatically creates a directory on a globus server as "year-month/pi_last_name" (or any other preset path) and sends a customizable notification email to "pi_email" that includes the URL to the shared folder.

year-month, pi_last_name and pi_email area automatically retrieved from the APS scheduling system for the current user (see `DTagging <https://github.com/decarlof/DTagging>`_ for more information on how to create and update epics process variables containing user and experiment information using the APS scheduling system).

`globus <https://github.com/decarlof/globus>`_ also creates automatically year_month/user folders on both data collection and data analysis machines (e.g. pg10ge and handyn) 

At the beginning of a new user beamtime login into user2bmb@arcturus then::

    start_tomo 

and open the user info screen:

.. image:: ../img/medm_screen.png 
   :width: 480px
   :align: center
   :alt: tomo_user

and make sure the user PV are updated correctly from the scheduling system if not hit the update button or manually enter the user last name/email address then::

    [user2bmb@arcturus]$ bash

to create YYYY-MM/PI_last_name directories on data collection and data analysis computers::

    [user2bmb@arcturus]$ globus dirs

to send a notification email to the experiment PI with the Globus link from where to downalod the data::

    [user2bmb@arcturus]$ globus email

to send the same to all users listed in the proposal::

    [user2bmb@arcturus]$ globus email --schedule


Full help::

    [user2bmb@arcturus]$ globus -h
    usage: globus [-h] [--config FILE]  ...

    optional arguments:
        -h, --help     show this help message and exit
        --config FILE  File name of configuration

    Commands:
  
        init         Create configuration file
        show         Show endpoints
        email        Create folder on endpoint and send email with link to user
        dirs         Create folders on data collection and data analysis computers


