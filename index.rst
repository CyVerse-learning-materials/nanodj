|CyVerse logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

Quick start of NanoDJ VICE app in DE
====================================

Goal
----

`NanoDJ <https://github.com/genomicsITER/NanoDJ/>`_ is a Dockerized Jupyter Notebook for interactive Oxford Nanopore MinION sequence manipulation and genome assembly. It integrates basecalling, read trimming and quality control, simulation and plotting routines with a variety of widely used aligners and assemblers, including procedures for hybrid assembly.

- Facilitate ONT sequence analyses by integrating capabilities for data manipulation, sequence comparison and assembly in field experiments or for educational purposes.

- Interactively explore your data with beautiful visualizations that provide new perspectives.

- Easily share results with your team, even those members without NanoDJ installed.

In this quick start, we will show you how to launch NanoDJ VICE app in DE.

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/TYXcEsCWGI0" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>
  
----

Prerequisites
-------------

Downloads, access, and services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this tutorial you will need access to the following services/software*

	.. list-table::
	    :header-rows: 1

	    * - Prerequisite
	      - Preparation/Notes
	      - Link/Download
	    * - CyVerse account
	      - You will need a CyVerse account to complete this exercise
	      - `Register <https://user.cyverse.org/>`_

----

Platform(s)
~~~~~~~~~~~

*We will use the following CyVerse platform(s):*

.. list-table::
    :header-rows: 1

    * - Platform
      - Interface
      - Link
      - Platform Documentation
      - Learning Center Docs
    * - Discovery Environment
      - Web/Point-and-click
      - `Discovery Environment <https://de.cyverse.org/de/>`_
      - `DE Manual <https://wiki.cyverse.org/wiki/display/DEmanual/Table+of+Contents>`_
      - `Guide <https://learning.cyverse.org/projects/discovery-environment-guide/en/latest/>`__

----

Input and example data
~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this quickstart you will need to have the following inputs prepared*. 

.. Note::

  The example input data (which contains data and Jupyter notebooks) is already prefilled for you during app launch

.. list-table::
    :header-rows: 1

    * - Input File(s)
      - Format
      - Preparation/Notes
      - Example Data
    * - Fast5 and Jupyter notebooks
      - - `Fast5 <http://bioinformatics.cvr.ac.uk/blog/exploring-the-fast5-format/>`_
        - Jupyter notebooks 
      - Input data can be a list of FAST5 files from previous basecalled runs (e.g. a Metrichor output) or event
        level signal data to be basecalled using the latest ONT caller
      - ``data_transfer.sh`` (Community Data -> iplantcollaborative -> example_data -> nanodj and select ``data_transfer.sh`` script)

-----

*Get started: Launch NanoDJ*
-----------------------------

1. Login to the |discovery_enviornment|.

2. Click on **Apps** window in the DE workspace and search for and run NanoDJ.

.. Tip::

  Alternatively you can clik this |nanodj logo|_ button to directly launch the NanoDJ VICE app.

3. Under “Analysis Name” leave the defaults or make any desired notes.

4. Under “Parameters” for ‘Input files', click the "+" and browse ``data_transfer.sh`` (iplantcollaborative > example_data > nanodj and select ``data_transfer.sh`` script).

5. Click **Launch Analysis**. You will receive couple of notifications on the bell corresponding to job submission and running with the "Access your running analysis here". 

6. Clicking on the "Access your running analysis" will open the NanoDJ JupyterLab in another tab in the browser after a brief building phase.

.. Note::

  You will be asked to authenticate again to the JupyterLab with your CyVerse username and password

7. Open the Terminal in the main JupyterLab interface (under 'others' section), navigate to the ``vice`` folder and execute the ``data_transfer.sh`` script to initiate the test data downloading process. You will be asked to enter your CyVerse password again to initiate the downloading process.

.. code-block:: bash

  cd vice
  bash data_transfer.sh
  Enter your current iRODS password:

8. Finally, once you finish analysis, navigate to the Discovery Environment tab, select the Analysis window and select the analysis, click "save and complete analysis". Upon clicking complete analysis, the analysis will be completed and all the outputs will be brought back to the analysis folder. Alternatively you can use ``iput -rPVT <folder name>`` command to transfer the data back to the data store.

.. Note::
  
  Currently quick starts uses a reduced test data but if you want to try the full test data, then instead of using ``data_transfer.sh``, use ``data_transfer_full.sh`` script which is in the same folder as the other script.

----

Additional information, help
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Full materials for the webinar is available `here <https://wiki.cyverse.org/wiki/pages/viewpage.action?pageId=45322621>`_

- See the original `JupyterLab quick start <https://learning.cyverse.org/projects/vice/en/latest/user_guide/quick-jupyter.html>`_ 

- See the original `NanoDJ <https://github.com/genomicsITER/NanoDJ>`_ for how to run ONT data analysis

- Search for an answer: `CyVerse Learning Center <http://learning.cyverse.org>`_ or `CyVerse Wiki <https://wiki.cyverse.org>`_

- Contact CyVerse support by clicking the intercom button on the page.

----

**Fix or improve this documentation**

- On Github: `Repo link <https://github.com/CyVerse-learning-materials/fastqc_quickstart>`_
- Send feedback: `Tutorials@CyVerse.org <Tutorials@CyVerse.org>`_

----

|Home_Icon|_
`Learning Center Home`_

.. |nanodj logo| image:: ./img/vice_badge.png
.. _nanodj logo: https://de.cyverse.org/de/?type=apps&app-id=b0e5bdc4-6226-11e9-a28f-008cfa5ae621&system-id=de

.. |CyVerse logo| image:: ./img/cyverse_rgb.png
    :width: 500
    :height: 100
.. _CyVerse logo: http://learning.cyverse.org/
.. |Home_Icon| image:: ./img/homeicon.png
    :width: 25
    :height: 25
.. _Home_Icon: http://learning.cyverse.org/
.. |discovery_enviornment| raw:: html

    <a href="https://de.cyverse.org/de/" target="_blank">Discovery Environment</a>