.. image:: https://img.shields.io/badge/sitcomtn--088-lsst.io-brightgreen.svg
   :target: https://sitcomtn-088.lsst.io/
.. image:: https://github.com/lsst-sitcom/sitcomtn-088/workflows/CI/badge.svg
   :target: https://github.com/lsst-sitcom/sitcomtn-088/actions/

##################
M1M3 Dynamic tests
##################

SITCOMTN-088
============

Linked with: SITCOM-948
This technote summarizes the results of the m1m3 dynamic tests including positioning during a slew and the settling time after a slew

**Links:**

- Publication URL: https://sitcomtn-088.lsst.io/
- Alternative editions: https://sitcomtn-088.lsst.io/v
- GitHub repository: https://github.com/lsst-sitcom/sitcomtn-088
- Build system: https://github.com/lsst-sitcom/sitcomtn-088/actions/

Build this technical note
=========================

You can clone this repository and build the technote locally if your system has Python 3.11 or later:

.. code-block:: bash

   git clone https://github.com/lsst-sitcom/sitcomtn-088
   cd sitcomtn-088
   make init
   make html

Repeat the ``make html`` command to rebuild the technote after making changes.
If you need to delete any intermediate files for a clean build, run ``make clean``.

The built technote is located at ``_build/html/index.html``.

Publishing changes to the web
=============================

This technote is published to https://sitcomtn-088.lsst.io/ whenever you push changes to the ``main`` branch on GitHub.
When you push changes to a another branch, a preview of the technote is published to https://sitcomtn-088.lsst.io/v.

Editing this technical note
===========================

The main content of this technote is in ``index.rst`` (a reStructuredText file).
Metadata and configuration is in the ``technote.toml`` file.
For guidance on creating content and information about specifying metadata and configuration, see the Documenteer documentation: https://documenteer.lsst.io/technotes.
