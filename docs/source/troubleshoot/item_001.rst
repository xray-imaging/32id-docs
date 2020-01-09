Bluesky time out error
======================

.. contents:: 
   :local:

If you get this time out error::

    <class 'str'>: (<class 'TimeoutError'>, TimeoutError('Failed to connect to mona:StopAcquisition',))


at the end of a scan using bluesky verify that the soft IOC providing the PV "mona:StopAcquisition" is up and running with::


    [user2bmb@lyra,47,startup]$ cd ~/.ipython/profile_2bmb/startup/
    [user2bmb@lyra,52,startup]$ caget mona:StopAcquisition

if you get::

    Channel connect timed out: 'mona:StopAcquisition' not found

then you need to start the soft IOC with::

    [user2bmb@lyra,47,startup]$ cd ~/.ipython/profile_2bmb/startup/
    
    screen
    softIoc -d mona.db
    keypresses: [^a] then [d]

and you will get::

    [user2bmb@lyra,46,startup]$ caget mona:StopAcquisition
    mona:StopAcquisition           Ok
