Globus is down
==============

All internal data transfer is handled by `Globus <https://www.globus.org>`_, if down make sure to
start the local `Globus EndPoint <https://www.globus.org/globus-connect-personal>`_ with:


hadyn
~~~~~

Log in as tomo@handyn::

    [tomo@handyn,~]$ cd ~/Software/globusconnectpersonal-2.3.5/
    [tomo@handyn,~]$ ./globusconnect

pg10ge
~~~~~~

Log in as user2bmb@pg10ge::

    [user2bmb@pg10ge]$ cd ~/globusconnectpersonal-2.3.6
    [user2bmb@pg10ge]$ ./globusconnectpersonal -status
    [user2bmb@pg10ge]$ ./globusconnectpersonal -stop
    [user2bmb@pg10ge]$ ./globusconnectpersonal -start &