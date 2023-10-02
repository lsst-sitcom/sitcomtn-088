:tocdepth: 1

.. sectnum::

.. Metadata such as the title, authors, and description are set in metadata.yaml

.. TODO: Delete the note below before merging new content to the main branch.

.. note::

   **This technote is a work-in-progress.**

Abstract
========

Linked with: SITCOM-948

This technote summarizes the results of the m1m3 dynamic tests including positioning stability before and after a slew and the settling time after a slew.

Requirements
------------

**LTS-88-REQ-0051**

**LTS-88-REQ-0052** 

Related SITCOM tickets
======================

SITCOM-797: `M1M3 - Slewing analysis - Positioning <https://jira.lsstcorp.org/browse/SITCOM-797>`__ 

SITCOM-798: `M1M3 - Settling time after a slew <https://jira.lsstcorp.org/browse/SITCOM-798>`__

SITCOM-797: M1M3 - Slewing analysis - Positioning
=================================================

Requirement verified
--------------------

**LTS-88-REQ-0052**: The positioning system SHALL maintain mirror decenter less than +/- 6 micrometer, mirror tilt less than +/- 24 e-6 degree, and piston less than +/- 1  micrometer, all relative to the mirror cell, after a slew of 3.5 degrees or less (short slew).

Test Case and Results
---------------------

See `SITCOMTN-084 <https://sitcomtn-084.lsst.io/>`__.

SITCOM-798: M1M3 - Settling time after a slew
=============================================

Requirement verified
--------------------

**LTS-88-REQ-0051**: The positioning system SHALL be able to
meet all its requirements within 3 seconds of ending a short
slew (3.5 degrees in 2 seconds)

*The requirement is for the system to have settled to the same (within accuracy) position after a short slew, within 3 seconds.*

Test Case
---------
`LVV-11258 <https://github.com/lsst-sitcom/notebooks_vandv/tree/tickets/SITCOM-798/notebooks/tel_and_site/subsys_req_ver/m1m3>`__ 

Plot the settling time of the M1M3 for X, Y, Z, RX, RY, and RZ.

The data comes from the EFD: imsData. The IMS is the
Independent Measurement System, a set of electronic
micrometers that measure the displacement of the M1M3 mirror
with respect to the cell. According to LTS-88 it has a 4 um
accuracy in XYZ and 3e-5 degree accuracy in RXRYRZ.

Test Data
---------
*Looked for suitable cases in Rubin TV. TBD a systematic search for those cases closest to the requirement settings (3.5 degree slew at full speed, not reached yet as far as I know as of 240823).*

- dayObs = 2023-06-27
- seqNo = 450
- Duration = 5s
- Azimuth only 3.5 degree slew

See `RubinTV <https://roundtable.lsst.codes/rubintv-dev/summit/tma/historical/2023-06-27>`__

Results
-------
IMS XYZ position with azimuth and elevation reference. Vertical line denotes reference time (slew stop):


.. figure:: /_static/xyz_vs_azel.png
   :name: fig-xyzvsazel

   IMS XYZ during the slew, compared to azimuth and elevation from mount information. 

RXRYRZ rotation with azimuth and elevation reference. Vertical line denotes reference time (slew stop):

.. figure:: /_static/rxryrz_vs_azel.png
   :name: fig-rxryrzvsazel

   IMS RXRYRZ during the slew, compared to azimuth and elevation from mount information.

Settling behavior from the IMS measurements. IMS values during and after slew, with RMS behavior with respect to end of the plot, with a 3 second requirement window .

.. figure:: /_static/xsettle.png
   :name: fig-xsettle

   IMS x residual compared to value at slew stop, RMS, in mm.

.. figure:: /_static/ysettle.png
   :name: fig-ysettle

   IMS y residual compared to value at slew stop, RMS, in mm.

.. figure:: /_static/zsettle.png
   :name: fig-zsettle

   IMS z residual compared to value at slew stop, RMS, in mm.

.. figure:: /_static/xrotsettle.png
   :name: fig-xrotsettle

   IMS rotation in x residual compared to value at slew stop, RMS, in degrees.

.. figure:: /_static/yrotsettle.png
   :name: fig-yrotsettle

   IMS rotation in y residual compared to value at slew stop, RMS, in degrees.

.. figure:: /_static/zrotsettle.png
   :name: fig-zrotsettle

   IMS rotation in z residual compared to value at slew stop, RMS, in degrees.




Related documents
=================
`M1M3 Mirror Support Design Requirement Document LTS-88 <https://docushare.lsst.org/docushare/dsweb/Get/LTS-88/LTS-88.pdf>`__

.. Make in-text citations with: :cite:`bibkey`.
.. Uncomment to use citations
.. .. rubric:: References
.. 
.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa
