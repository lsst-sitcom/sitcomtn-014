.. image:: https://img.shields.io/badge/sitcomtn--014-lsst.io-brightgreen.svg
   :target: https://sitcomtn-014.lsst.io
.. image:: https://github.com/lsst-sitcom/sitcomtn-014/workflows/CI/badge.svg
   :target: https://github.com/lsst-sitcom/sitcomtn-014/actions/

#########################################
Project Documentation Future State Report
#########################################

SITCOMTN-014
============

This technical note is a report to recommend a future state for Rubin Observatory Operations documentation by the Project-wide Documentation Working Group. This proposal presents a high-level documentation strategy for Rubin Observatory Operations with suggested methodologies to transition Construction Project documents and organizations for the technical documentation package needed to establish construction completeness and operational readiness. It responds to charge item 3 in the Charge to the Documentation Working Group, LSE-489. Migration plans, schedule and resources to migrate to the future state for this documentation will be reported in another technical report, RTN-076. Implementation of this proposal (or its equivalent) is a key deliverable from the Rubin Observatory Construction Project to Operations.

Links
=====

- Live drafts: https://sitcomtn-014.lsst.io
- GitHub: https://github.com/lsst-sitcom/sitcomtn-014

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-sitcom/sitcomtn-014

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
