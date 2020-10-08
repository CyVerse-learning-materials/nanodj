.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

Quick start of NanoDJ VICE app in DE
====================================

Goal
----

|Nano DJ| is a Dockerized Jupyter Notebook for interactive Oxford Nanopore MinION sequence manipulation and genome assembly. It integrates basecalling, read trimming and quality control, simulation and plotting routines with a variety of widely used aligners and assemblers, including procedures for hybrid assembly.

- Facilitate ONT sequence analyses by integrating capabilities for data manipulation, sequence comparison and assembly in field experiments or for educational purposes.

- Interactively explore your data with beautiful visualizations that provide new perspectives.

- Easily share results with your team, even those members without NanoDJ installed.

In this quick start, we will show you how to launch NanoDJ VICE app in DE.

|nanodj webinar|
  
----

Manual Maintainer(s)
------------------------

Who to contact if this manual needs fixing. You can also email
`Tutorials@CyVerse.org <Tutorials@CyVerse.org>`_

.. list-table::
    :header-rows: 1

    * - Maintainer
      - Institution
      - Contact
   * - Amanda Cooksey
      - CyVerse / UA
      - amandamcooksey@gmail.com

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
      - |CyVerse User Portal|

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
      - |Discovery Environment|
      - |DE Manual|
      - |Discovery Environment Guide|

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
      - - |fast5|
        - Jupyter notebooks 
      - Input data can be a list of FAST5 files from previous basecalled runs (e.g. a Metrichor output) or event
        level signal data to be basecalled using the latest ONT caller
      - Community Data > cyverse_training > quickstarts > nanodj

-----

*Get started: Launch NanoDJ*
-----------------------------

1. Login to the |Discovery Environment|.

2. Click on **Apps** window in the DE workspace and search for and run NanoDJ.

.. Tip::

  Alternatively you can clik this |nanodj launch| button to directly launch the NanoDJ VICE app.

3. Under “Analysis Name” leave the defaults or make any desired notes.

4. Under “Parameters” for ‘Input files', click the "+" and browse ``data_transfer.sh`` (Community Data > cyverse_training > quickstarts > nanodj and select ``data_transfer.sh`` script).

5. Click **Launch Analysis**. You will receive couple of notifications on the bell corresponding to job submission and running with the "Access your running analysis here". 

6. Clicking on the "Access your running analysis" will open the NanoDJ JupyterLab in another tab in the browser after a brief building phase.

7. Open the Terminal in the main JupyterLab interface (under 'other' section), navigate to the ``vice`` folder and execute the ``data_transfer.sh`` script to initiate the test data downloading process. You will be asked to enter your CyVerse password again to initiate the downloading process.

.. code-block:: bash

  cd vice
  bash data_transfer.sh
  Enter your current iRODS password:

.. Tip::

   Alternatively you can import your own data using iCommands in terminal or by connecting to your CyVerse Data Store. To connect to your Data Store click on the CyVerse icon on the left side of the JupyterLab workspace and login using your CyVerse credentials.

8. To run the 'demo' analysis close the terminal window and access the notebooks by clicking on the folder icon and navigating to vice > nanodj_webinar_demo. From here you can access each notebook required for the analysis.

9. Finally, once you finish your analysis, navigate back to the Discovery Environment, select the analysis in the Analysis window and click "save and complete analysis" under the ellipsis menu. Upon clicking complete analysis, the analysis will be completed and all the outputs will be brought back to the analysis folder. Alternatively you can use ``iput -rPVT <folder name>`` command to transfer the data back to the data store.

.. Note::
  
  Currently the quickstart uses a reduced test dataset but if you want to try the full test dataset, then instead of using ``data_transfer.sh``, use ``data_transfer_full.sh`` script which is in the same folder as the other script.

----

Additional information, help
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- See the original |jupyterlab quick start| 

- See the original |Nano DJ| GitGub for how to run ONT data analysis

----

**Fix or improve this documentation**

- Search for an answer:
  |CyVerse Learning Center|
- Ask us for help:
  click |Intercom| on the lower right-hand side of the page
- Report an issue or submit a change:
  |Github Repo Link|
- Send feedback: `Tutorials@CyVerse.org <Tutorials@CyVerse.org>`_

----
