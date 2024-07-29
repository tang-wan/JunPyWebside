.. Junpy Webside documentation master file, created by
   sphinx-quickstart on Wed Jul 24 14:04:00 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Junpy Webside
===========================

.. figure:: /Figure/JunpyIcon.png

Here is the *home* *page* of **Junpy** Webside.

Introduction
---------------
JunPy is a Python package for spin transport calculation within the framework of non-equilibrium Green's function method (NEGF).
It serves as post analysis tools of first principles calculation under two-probes device to calculate:

#. Transmission
#. Current
#. Density of states
#. Spin torque.

Feature
---------
* **Based on Python3 and C++**
* **Spin calculate with non-equilibrium Green's function method (NEGF)**
   * Current, transmission, dos
   * Single -band tight-binding model
   * Combine first-principles calculation
* **Open source**
   * General public license (GPL)
* **User and developer friendly**
   * Online manual
   * Rich examples
* **Performance issues**
   * High performance library: `Numpy <https://numpy.org/>`_ and `ScyPy <https://scipy.org/>`_
   * Using symmetry k-points (using spglib)
   * Parallel computing with MPI (using mpi4py)
   * Combine C++ directly

[IGNORE]
---------
If anyone want to learn more about **Junpy**, you can read the following content.

If you want to use Junpy you can just ``import jumpy as jp`` so that you can use **Junpy** in python as ``jp.[function]``.

Roughly, **Junpy** can calculate following things:



.. Tip::
   This package need to use with `nanodcal <https://docs.nanoacademic.com/nanodcal/#>`_. Because it will use the hamitonian which is calculated by nanodcal

.. danger:: 
   This package is pretty good. Please be careful not to become overly addicted


.. In toctree, you can use ":hidden:" to hide the hyperlink in home
.. toctree::
   :maxdepth: 2
   :caption: Guildlines:

   Guildline/1_Installation.rst
   Guildline/2_Tutorial.rst
   Guildline/3_Example.rst
   Guildline/4_InputReference

.. toctree::
   :maxdepth: 2
   :caption: Appendix:
   
   Appendix/5_Theorem
   Appendix/6_ContactUs
   Appendix/7_Forum

.. caution:: 
   This Webside is still building, and Source codes of JunPy are going to be opened in the future.
   JunPy is still in development and temporarily unavailable in public.
   If you have some ideas and questions, please :doc:`contact us </Appendix/6_ContactUs>`