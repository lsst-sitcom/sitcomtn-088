#####################
Summary of M1M3 Tests
#####################

.. TODO: Delete the note below before merging new content to the main branch.
.. note::

   **This technote is a work-in-progress.**

.. abstract::
   This technote summarizes the M1M3 dynamic tests and corresponding technotes in the context of glass safety as of June 4th 2024.


Introduction
============

This technote summarizes the M1M3 dynamic tests in the context of Glass Safety. It will be periodically updated with new results. The current technote corresponds to status as of June 4th 2024. A list of technotes with their updated dates and associated data sets is provided below. Following that, the list is broken down into thematic sections on different aspects of M1M3 Glass Safety and a summary of current results and next steps is provided.


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

* `SITCOMTN-079 <https://sitcomtn-079.lsst.io/>`_ **M1M3 Iterative Improvement of LUT Through Balance Forces**

  *Results*: After the improvements made in July 2023 to the Look-Up Table (LUT), the hardpoint measured forces have been minimized. The “rule of thumb” for the LUT is that we should expect about 1/1000 correction. Our mirror weighs 170,000 N. We should expect to get within 170N. It looks like we are within this range.

  *Pending tasks*: To further improve the LUT, tests could be performed to validate that we have reached convergence and the LUT includes all the gravitational loads dependency.

* `SITCOMTN-092 <https://sitcomtn-092.lsst.io/v/SITCOM-1081/index.html>`_ **M1M3 Force Balance System - Inertia Compensation**

  *Results*: After applying different forces at 10% to 100% performance, maximum are occasionally seen at above 1000N, whereas the limit currently stands at 900 N.

  *Pending tasks*: Update technote to reflect most recent results (shown at the Glass Safety review) and merge into main. Define next steps, and possible risk minimization. Technote format is old. There is a ticket (`SITCOM-1463 <https://sitcomtn-092.lsst.io/v/SITCOM-1463/index.html>`) with the new format but although this ticket is "done", the information does not appear.

* `SITCOMTN-107 <https://sitcomtn-107.lsst.io/>`_ **M1M3 Actuator Delays and Following Errors**

  *Results*: For aggressive slews, the measured forces do not track the applied forces well at all. So it appears that the problem with large hardpoint forces for the aggressive slews is more serious than just time delays.

  *Pending tasks*:  We need to understand why the measured forces are deviating so strongly from the intended forces.

Bump tests
----------
* `SITCOMTN-083 <https://sitcomtn-083.lsst.io/>`_ **M1M3 Mirror Cell Bump Testing**

  *Results*: Bump tests have been performed throughout several months. Map of failures per actuator were created, together with typical failure modes (mostly on Z axis), for ~200 N bump tests.
  Actuators showed a higher failure rate when pushing the mirror up, with larger deviations in the positive direction.
  Importantly, for failed actuators no worsening trend over time was observed. Latency between actual and demanded forces was marginal.
  Forces overshot in 23% and undershot in 73% of bump test executions.
  
  *Pending tasks*:  Establish a failure probability measure.
  Actuators passing the bump test may need to publish measured forces in the EFD for continuous monitoring, enabling early detection of potential failures.
  Additionally, define action plans based on the current data and requirements other than 'not fault'.

Hardpoint tests
---------------
* `SITCOMTN-081 <https://sitcomtn-081.lsst.io/v/SITCOM-918/index.html>`_ **M1M3 Hardpoint Oscillations During Elevation Slews**

  *Results*: Evidence shown for oscillatory behavior during elevation and azimuth slews, by measuring hardpoint forces and identifying events above a 100 N threshold.  Analysis of a one-off event started by TMA in June 2023 demonstrated no apparent coupling to M1M3.
  The technote has been updated with an analysis of the oscillations during elevation slews for a period from April 2023 to June 2023. The tests show small oscillations of unknown origin (as of September 2024) but which do not appear to compromise the hardpoint limits. 
  In addition, an analysis of earthquake events has been performed. However, the data are inconclusive since on the days analyzed it was not possible to compare the hardpoint forces along the same axes and compare them with the accelerations because the telescope was stationary.

  *Pending tasks*: Pending a more systematic analysis of earthquake behavior because it could not be done with the existing data at the time. 

* `SITCOMTN-082 <https://sitcomtn-082.lsst.io/>`_ **M1M3 Hardpoint Breakaway** 

  *Results*:  Breakaway system works in general. Some notable exceptions (HP2, HP5 breakaway system faults at low (<30 deg) elevations, response shape also different) seem to be have an explanation according to Yijung and Petr. The format of the technical notes is in the new format (SITCOM-1111-2 dated 2024-01-23). However, these updates are not shown in the “Current” version which is in the old format. The technical note SITCOM-111-2 contains more explanations and conclusions than the current one.

  *Pending tasks*: Update to “current” the latest version of tecnote and perform the tasks indicated in requirements in verification. 


Stability tests
---------------
* `SITCOMTN-084 <https://sitcomtn-084.lsst.io/>`_ **M1M3 Position Repeatability Analysis**

  *Results*: The initial specifications on the mirror positions and rotations are not met, especially for the piston (z displacement). After discussion with experts, it was realized that these displacements are normal and correspond to the sag of the mirror cell due to gravity change that should be compensated by adjusting the M2 and camera hexapods. However this procedure does not seem to counteract the effect at the required level. For az only movements,  the mirror displacements are within the specifications but for the rotation around the x axis where there are some outliers. The mirror rotation seems also correlated to the azimuth difference for movement < 50 degrees. For larger TMA movements the mirror rotation is within the specifications. Raise/park repeatability is verified as well.

  *Pending tasks*: Confirmation of the observed behavior with higher statistics. Study how to reduce the scatter for the correction in Z through adjustments of M2 and hexapods.

* `SITCOMTN-095 <https://sitcomtn-095.lsst.io/>`_ **M1M3 Settling Time After a Slew**
  
  *Results*: The requirement is failed using a threshold of 5 seconds after slew start due to a failure in the yPosition and yRotation columns predominantly, due to a slow drift of the cell. However, in a large majority of cases settling happens in < 2 s later and just barely misses the requirement for the system. NB that we have included RMS and bias of the IMS value, despite not being strictly the specification, as we considered it relevant to highlight these slow drifts that may not incur in any jittering at all.

  *Pending tasks*: Repeat analysis with updated adjustments to commands (which could be fixing the errors) when mirror is in place. Technote format is old.

* `SITCOMTN-109 <https://sitcomtn-109.lsst.io/>`_ **M1M3 Analyze position and rotation stability throughout a tracking period**

  *Results*: After analyzing all the two-night tracking we have seen that the mirror remains stable.  The duration of the tracking is 42 seconds and not 30 seconds as initially indicated.

  *Pending tasks*: Figure out what is going on with the 42 s 'observing' period. 

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
