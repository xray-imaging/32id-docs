FDT data transfer
=================

.. contents:: 
   :local:

To copy data from windows (ex.: S:\data\2019-02\user_name\test.h5) to linux  (ex.: /local/data/user_name/) first install FDT (http://monalisa.cern.ch/FDT/ on both machines then go to the linux machine start the fdt server::

    $ cd /local/data/fdt
    $ java -jar fdt.jar

then go to the windows machine from a dos prompt start the copy (client)::

    $ cd C:\Users\se2admin\Desktop\FDT\
    $ java -jar fdt.jar -c handyn -d /local/data/Dunand/ S:\data\2019-02\Dunand\test.h5
