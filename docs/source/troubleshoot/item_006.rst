sublime editor
==============

.. contents:: 
   :local:

if the sublime editor fails to start with::

    user2bmb@pg10ge$ sublime


is because there is another session opened remotely. To kill it::

    user2bmb@pg10ge$ ps -A | grep sublime

to find the sublime's process id # (ex. 12345), then::

    user2bmb@pg10ge$ kill -9 12345
    user2bmb@pg10ge$ sublime
