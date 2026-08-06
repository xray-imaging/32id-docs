===============
Data Management
===============

This page summarizes the DM (APS Data Management) status for 32-ID datasets.

Convention: **Done** means the dataset was permanently moved from ``/data2/32ID`` or
``/data3/32ID`` to ``/gdata/dm/32ID`` and the original copies were deleted.
**Pending** means the dataset still lives on one of the local disks and has not yet
been fully archived / deletion authorization is not yet given.

.. contents:: On this page
   :local:
   :depth: 2


Done — permanently on DM
========================

.. list-table::
   :header-rows: 1
   :widths: auto

   * - Dataset
     - Size
     - Removed from
     - DM location
   * - ``2026-07-Allen-1013067`` (raw + rec)
     - 20 T
     - /data3/32ID/2026-07-Allen-1013067{,_rec}
     - /gdata/dm/32ID/2026-07/2026-07-Allen-1013067/{data,analysis}/
   * - ``2026-07-Forien-1020121`` (raw + rec)
     - 1.67 T
     - /data2/32ID/2026-07-Forien-1020121{,_rec}
     - /gdata/dm/32ID/2026-07/2026-07-Forien-1020121/{data,analysis}/
   * - ``2026-07-Li-1015453`` (raw + rec on /data2, rec only on /data3)
     - 1.27 T (data2) + 2.3 T (data3 rec)
     - /data2 and /data3/32ID/2026-07-Li-1015453{,_rec}
     - /gdata/dm/32ID/2026-07/2026-07-Li-1015453/{data,analysis}/
   * - ``2026-07-Mittone-1015453``
     - 11 G
     - /data3/32ID/2026-07-Mittone-1015453
     - /gdata/dm/32ID/2026-07/2026-07-Fezzaa-1021154/data/  *(re-homed to Fezzaa GUP)*
   * - ``2026-07-Scharnagl-1015240`` (raw + rec)
     - 1.31 T
     - /data2/32ID/2026-07-Scharnagl-1015240{,_rec}
     - /gdata/dm/32ID/2026-07/2026-07-Scharnagl-1015240/{data,analysis}/
   * - ``2026-07-Wadehra-1015147`` (raw + rec)
     - 861 G
     - /data2/32ID/2026-07-Wadehra-1015147{,_rec}
     - /gdata/dm/32ID/2026-07/2026-07-Wadehra-1015147/{data,analysis}/
   * - ``2026-07-Zhu-1017678`` (raw + rec)
     - 764 G
     - /data3/32ID/2026-07-Zhu-1017678{,_rec}
     - /gdata/dm/32ID/2026-07/2026-07-Zhu-1017678/{data,analysis}/


Pending — still on local disk, not fully archived
=================================================

.. list-table::
   :header-rows: 1
   :widths: auto

   * - Dataset / Path
     - Size
     - DM status
     - Action needed
   * - ``/data2/32ID/2026-07-Nikitin/``
     - 481 G
     - fully on DM as ``2026-07-Mokso-1022117/data/probe_calibration/``
     - keep for continued processing; safe to delete when finished
   * - ``/data2/32ID/2026-07-Nikitin-1015240/``
     - 691 G
     - fully on DM as ``2026-07-Mokso-1022117/data/tomography/``
     - keep for continued processing; safe to delete when finished
   * - ``/data2/32ID/2026-07-Nikitin-1015240_rec/``
     - 275 G
     - fully on DM as ``2026-07-Mokso-1022117/analysis/``
     - keep for continued processing; safe to delete when finished
   * - ``/data2/32ID/Xiaoyang`` + ``Xiaoyang_rec``
     - 3.1 T (2.0 + 1.1)
     - **no DM home identified**
     - identify owner / target GUP or delete
   * - ``/data2/32ID/Peter`` + ``Peter_rec``
     - 2.4 T (605 G + 1.8 T)
     - **no DM home identified**
     - identify owner / target GUP or delete
   * - ``/data2/32ID/CORML``
     - 276 M
     - undated, DM home unknown
     - assess

Mokso-Nikitin folder mapping (kept locally on /data2)
-----------------------------------------------------

Viktor Nikitin's holotomography experiment lives on ``/data2/32ID`` under folder
names starting with ``2026-07-Nikitin*`` for continued processing, but on DM it is
archived under GUP **1022117 — PI: Rajmund Mokso** (proposal: *"A new
holotomographic scheme with multilayer laue lenses"*, 2026-07-31 to 2026-08-05).

.. list-table::
   :header-rows: 1
   :widths: auto

   * - /data2/32ID source
     - DM destination under ``2026-07-Mokso-1022117``
   * - ``2026-07-Nikitin/`` *(probe/calibration — 90 h5, no configs)*
     - ``data/probe_calibration/``
   * - ``2026-07-Nikitin-1015240/`` *(tomography raw, .h5 + .config)*
     - ``data/tomography/``
   * - ``2026-07-Nikitin-1015240_rec/`` *(per-slice tiff reconstructions)*
     - ``analysis/``

Additional metadata on DM under ``2026-07-Mokso-1022117/data/``:

- ``control_software/`` — 11 scripts from Viktor's ``ca_modeling/`` (scan-trigger + probe scans + tomo scan + H5 metadata utilities)
- ``tomoscan/`` — coded-aperture piezo position files (``positions_x_20260804-201822.txt`` etc.) and per-projection piezo x,y tables for the tomo scans
- ``tomography/`` — plus per-projection piezo files (``step1b_*_piezo_x_y.txt``) alongside their matching h5s
