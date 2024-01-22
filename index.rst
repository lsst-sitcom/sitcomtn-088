##################
M1M3 Dynamic tests
##################

.. abstract::
   This technote is linked with: `SITCOM-948 <https://jira.lsstcorp.org/browse/SITCOM-948>`_

   This technote summarizes the results of the M1M3 dynamic tests.
   It contains an overall explanation of how the M1M3 system work.
   In addition, it serves as an index to the other tech notes produced on each test or data analysis.
   That includes tests like: Bump Test, Hard Point Breakaway Test, Settling Time, Positioning Repeatability,
   Force Balance System at different elevations, Inertia Compensation System performance,
   and deep study on vibrations.


.. TODO: Delete the note below before merging new content to the main branch.

.. note::

   **This technote is a work-in-progress.**


Introduction
============

.. todo:
      Add a brief introduction to the topic of this technote.

M1M3 Performance Analysis Tech Notes
====================================

* `SITCOMTN-081 <https://sitcomtn-081.lsst.io/>`_ M1M3 Hardpoint oscillations during elevation slews
* `SITCOMTN-082 <https://sitcomtn-082.lsst.io/>`_ M1M3 Hard Point Breakaway Analysis
* `SITCOMTN-083 <https://sitcomtn-083.lsst.io/>`_ M1M3 mirror cell bump testing
* `SITCOMTN-084 <https://sitcomtn-084.lsst.io/>`_ M1M3 Position Repeatability Analysis
* `SITCOMTN-092 <https://sitcomtn-092.lsst.io/>`_ M1M3 Force Balance System - Inertia Compensation
* `SITCOMTN-095 <https://sitcomtn-095.lsst.io/>`_ M1M3 Settling time after a slew


Requirements
------------

For all the tests, the requirements are extracted from the following document:

* `LTS-88 <https://ls.st/LTS-88>`_ M1M3 Mirror Support Design Requirements Document

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

*The requirement is for the system to have settled to the same (within precision) position after a short slew, within 3 seconds.*

Test Case and Results
---------------------

See `SITCOMTN-095 <https://sitcomtn-095.lsst.io/>`__.

Related documents
=================

`M1M3 Mirror Support Design Requirement Document LTS-88 <https://docushare.lsst.org/docushare/dsweb/Get/LTS-88/LTS-88.pdf>`__

.. Make in-text citations with: :cite:`bibkey`.
.. Uncomment to use citations
.. .. rubric:: References
..
.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa