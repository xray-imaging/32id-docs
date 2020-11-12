Sample alignment
================

| In order to align the sample on the center of rotation of the rotary stage and on the focal plan of the zone plate (objective lens) where X-ray are condensed, 4 motorized axis are needed:
| • **Sample Y** (vertical motion)
| • **Sample X** (horizontal motion perpendicular to the beam)
| • **Sample top X** (horizontal motion above the rotary stage)
| • **Sample top Z** (horizontal motion normal to "sample top X" above the rotary stage)

.. image:: img_guide/Sample_stack_coordinates.png
   :width: 1200px
   :align: center
   :alt: project

| 
| Below is a zoom on the graphical user interface portion related to those axis.
.. image:: img_guide/GUI_control_stages.png
   :width: 1200px
   :align: center
   :alt: project

| **Warning**: "Sample_X" and "Sample_Y" are air bearing stages. To actuate them, the air pressure of those stages needs to be turned ON by software.

| When the rotary stage is at 0\ :sup:`o`, "sample top X" and "sample top Z" are respectively perpendicular and parallel to the beam.
| To align the sample on the rotation axis, follow the 4 steps as described on the figure below:

.. image:: img_guide/Sample_alignment.png
   :width: 1200px
   :align: center
   :alt: project

| **Note**: "Sample_X" is used to align the center of rotation in respect to the beam, not to align samples on the rotation axis. While aligning the sample vertically, some parasitic motions might detune "Sample_X" by ~+/- 2 μm. Therefore, it is expected to realign Sample_X from one sample to another but only within ~4 μm range.
