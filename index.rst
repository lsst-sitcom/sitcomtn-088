#####################
Summary of M1M3 Tests
#####################

.. TODO: Delete the note below before merging new content to the main branch.
.. note::

   **This technote is a work-in-progress.**

.. abstract::
   This technote summarizes the M1M3 dynamic tests in the context of glass safety. It will be periodically updated with new results. The current technote corresponds to status as of June 4th 2024.


Introduction
============

Related tickets
===============
This technote is linked with: 

* `SITCOM-948 <https://jira.lsstcorp.org/browse/SITCOM-948>`_

* `SITCOM-1315 <https://jira.lsstcorp.org/browse/SITCOM-1315>`_

* `SITCOM-1380 <https://jira.lsstcorp.org/browse/SITCOM-1380>`_

M1M3 Performance Analysis
=========================
Index of tests and verification
-----------------------------------

.. list-table::
   :widths: 90 70 70
   :header-rows: 1

   * - Data taken on
     - Latest revision
     - Results presented in

   * -
       | 31 May 2023
     - | 24 July 2023
     - SITCOMTN-079 

   * -
       | 31 May 2023 -
       | 27 June 2023
     - | 25 March 2024
     - SITCOMTN-081 

   * -
       | 26 May 2023 -
       | 20 June 2023
     - | 17 November 2023
     - SITCOMTN-082

   * -
       | 01 November 2023 -
       | 15 January 2024
     - | 31 May 2024
     - SITCOMTN-083 

   * -
       | 10 January 2024 -
       | 12 January 2024
     - | 30 January 2024
     - SITCOMTN-084

   * -
       | TBC
     - | 02 November 2023
     - SITCOMTN-092

   * -
       | 20 December 2023
     - | 25 February 2024
     - SITCOMTN-095

   * -
       | 20 December 2023 -
       | 22 December 2023
     - | 18 March 2024
     - SITCOMTN-107 

   * -
       | 04 January 2024
       | 06 January 2024
     - | 01 March 2024
     - SITCOMTN-109 


Force balance tests
-------------------

* `SITCOMTN-079 <https://sitcomtn-079.lsst.io/v/SITCOM-1111/index.html>`_ M1M3 Iterative Improvement of LUT Through Balance Forces

  *Results*: After the improvements made in July 2023 to the Look-Up Table (LUT), the hardpoint measured forces have been minimized. The “rule of thumb” for the LUT is that we should expect about 1/1000 correction. Our mirror weighs 170,000 N. We should expect to get within 170N. It looks like we are within this range.

  *Pending tasks*: To further improve the LUT, tests could be performed to validate that we have reached convergence and the LUT includes all the gravitational loads dependency. Merge latest version of technote into main.

* `SITCOMTN-092 <https://sitcomtn-092.lsst.io/v/SITCOM-1081/index.html>`_ M1M3 Force Balance System - Inertia Compensation

  *Results*: After applying different forces at 10% to 100% performance, maximum are occasionally seen at above 1000N, whereas the limit currently stands at 900 N.

  *Pending tasks*: Update technote to reflect most recent results (shown at the Glass Safety review) and merge into main. Define next steps, and possible risk minimization. 

* `SITCOMTN-107 <https://sitcomtn-107.lsst.io/>`_ M1M3 Actuator Delays and Following Errors

  *Results*:

  *Pending tasks*:

Bump tests
----------
* `SITCOMTN-083 <https://sitcomtn-083.lsst.io/>`_ M1M3 Mirror Cell Bump Testing

  *Results*:

  *Pending tasks*:

Hardpoint tests
---------------
* `SITCOMTN-081 <https://sitcomtn-081.lsst.io/>`_ M1M3 Hardpoint Oscillations During Elevation Slews

  *Results*:

  *Pending tasks*:

* `SITCOMTN-082 <https://sitcomtn-082.lsst.io/>`_ M1M3 Hardpoint Breakaway 

  *Results*:

  *Pending tasks*:

Stability tests
---------------
* `SITCOMTN-084 <https://sitcomtn-084.lsst.io/>`_ M1M3 Position Repeatability Analysis

  *Results*:

  *Pending tasks*:

* `SITCOMTN-095 <https://sitcomtn-095.lsst.io/>`_ M1M3 Settling Time After a Slew
  
  *Results*:

  *Pending tasks*:

* `SITCOMTN-109 <https://sitcomtn-109.lsst.io/>`_ M1M3 Analyze position and rotation stability throughout a tracking period

  *Results*:

  *Pending tasks*:

Requirements
------------

For all the tests, the requirements are extracted from the following document:

* `LTS-88 <https://ls.st/LTS-88>`_ M1M3 Mirror Support Design Requirements Document


Related documents
=================

`M1M3 Mirror Support Design Requirement Document LTS-88 <https://docushare.lsst.org/docushare/dsweb/Get/LTS-88/LTS-88.pdf>`__
`Glass safety review <https://docs.google.com/presentation/d/1HmmzIUt0XszK0XMS1YZtQiYCvdwajhrZ8p3ZdAVSp14/edit#slide=id.p>`__

.. Make in-text citations with: :cite:`bibkey`.
.. Uncomment to use citations
.. .. rubric:: References
..
.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa