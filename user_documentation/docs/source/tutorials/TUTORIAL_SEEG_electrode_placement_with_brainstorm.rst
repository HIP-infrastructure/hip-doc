SEEG electrode placement with Brainstorm
*****************************************

.. figure:: /art/tutorial_seeg_placement_brainstorm_header.png
	:width: 600px
	:align: center

	**3D visualization of SEEG electrodes.** *SEEG electrodes have been generated and placed using* :doc:`Brainstorm</applications/APP_Brainstorm>` *.*

Disclaimer
==========

The methods and softwares used in this tutorial have not been certified for clinical practice and should be considered for 
research purposes only.  

About this tutorial
====================

Objective
---------

The objective of this tutorial is to guide HIP users in placing SEEG electrodes on a post-implantation volume using Brainstorm.

This tutorial consists of 2 parts which cover :ref:`the preparation of the working environment <prepare_environment_SEEG_placement_brainstorm>` and
:ref:`the placement of SEEG electrodes<place_SEEG_brainstorm>` 

Scope 
-----

This tutorial illustrates the minimal steps to place SEEG electrodes using Brainstorm on the HIP
and primarly consists of a video demonstration backed with a brief description of the performed steps.
This tutorial should be viewed as a starter guide as it does not go into all the intricacies of SEEG electrode placement.

For more in-depth information regarding the placement of SEEG electrodes using Brainstorm
please refer to the following official tutorials:

	* `Brainstorm's "Editing implantation without recordings" tutorial <https://neuroimage.usc.edu/brainstorm/Tutorials/Epileptogenicity#Editing_implantation_without_recordings>`_   
	* `Brainstorm's "Edit the contacts positions" tutorial <https://neuroimage.usc.edu/brainstorm/Tutorials/Epileptogenicity#Edit_the_contacts_positions>`_

Requirements
------------

There are no techincal requirements to follow this tutorial as the needed dataset and software are available on the HIP.

HIP software used in this tutorial:

	* :doc:`Brainstorm</applications/APP_Brainstorm>` (07-Jan-2022)

HIP dataset used in this tutorial:

	* :doc:`Epimap tutorial dataset</datasets/DATASET_Epimap>` (rev1.0)
	
.. _prepare_environment_SEEG_placement_brainstorm:

Prepare the working environment
==================================

**Get the dataset**: This tutorial relies on data available in the :doc:`Epimap tutorial dataset </datasets/DATASET_Epimap>`
which can be accessed in the corresponding `publicly shared folder <https://thehip.app/apps/files/?dir=/HIP%20tutorials/Epileptogenicity%20map%20computation%20with%20Brainstorm/Datasets&fileid=682152>`_.

A single file will be used for this tutorial:

	* anat/MRI/3DT1post_deface.nii

Transfer it into your private space so it is easier to access and use it.
If you don't know how to do this please refer to the :doc:`How to use the HIP spaces </guides/GUIDE_How_to_use_the_HIP_spaces_and_share_data_with_other_users>` guide.

**Start a new working session with Brainstorm**: This tutorial only requires the use of :doc:`Brainstorm</applications/APP_Brainstorm>`
for the placement of SEEG electrodes. It is advised to initiate a new working sesssion with a fresh instance of Brainstorm running.
If you don't know how to do this please refer to the :doc:`How to use the application library and working sessions </guides/GUIDE_How_to_use_the_application_library_and_working_sessions>` guide.

.. _place_SEEG_brainstorm:

Place SEEG electrodes with Brainstorm
=======================================

The accurate placement of SEEG electrodes requires some knowledge and a good understanding of the implantation procedure
(an implantation scheme or equivalent), of the type of material that has been implanted (SEEG electrode type/characteristics),
and some expertise in brain anatomy. 
It is also important to work on a high-resolution CT scan or T1 MRI scan acquired after the implantation of the depth electrodes so
the recording contacts appear either in hypersignal or hyposignal.

For confidentiality reasons, the implantation scheme will not be disclosed for this tutorial and the video demonstration focuses on the technical
procedure in order to place SEEG electrodes and generate a standardized implantation file using Brainstorm.


.. raw:: html

   <center>	
   <video width="680"  poster="https://thehip.app/apps/sharingpath/aboyer/Public/Tutorial%20-%20SEEG%20electrode%20placement%20with%20Brainstorm/Videos/HIP%20Tutorial%20-%20Thumbnail%20-%20SEEG%20electrode%20placement%20with%20Brainstorm.png" controls>
   <source src="https://thehip.app/apps/sharingpath/aboyer/Public/Tutorial%20-%20SEEG%20electrode%20placement%20with%20Brainstorm/Videos/HIP%20Tutorial%20-%20SEEG%20electrode%20placement%20with%20Brainstorm.mp4" type="video/mp4">
   Your browser does not support the video tag.
   </video>
   </center>

|

	


