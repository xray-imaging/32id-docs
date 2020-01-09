Bluesky
=======

.. contents:: 
   :local:

To operate 2-BM using bluesky type::

    user2bmb@lyra$ use_bluesky.sh 2bmb

Once in the ipython shell type::

    RE(user_tomo_scan(), comment="my tomo fly scan", sample="wood stick")

or::

    RE(user_tomo_scan(acquire_time=0.1), comment="my tomo fly scan", sample="wood stick")
    RE(user_tomo_scan(acquire_time=0.1, iteration=10), comment="my tomo fly scan", sample="wood stick")

