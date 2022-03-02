Epileptogenicity map computation with Brainstorm
**************************************************

.. figure:: /art/tutorial_epileptogenicity_header.png
	:width: 600px
	:align: center

	**Epileptogenicity map.** *Epileptogenicity map computed and visualized using* :doc:`Brainstorm</applications/APP_Brainstorm>` *.*

Disclaimer
==========

The methods and softwares used in this tutorial have not been certified for clinical practice and should be considered for 
research purposes only.  

About this tutorial
====================

Objective
---------

The objective of this tutorial is to guide HIP users in computing maps of epileptogenicity from ictal iEEG recordings.

Epileptogenicity maps show the spatial distribution, and eventually the temporal progression,
of the Epileptogenicity Index (EI) in the subject's brain.
The EI, is based on both spectral and temporal properties of iEEG signals
and quantifies the presence of high-frequency oscillations also referred as *rapid discharges*.
*Rapid discharges* have long been recognized as a characteristic electrophysiological pattern of the epileptogenic zone
and can help identify brain regions generating seizures ([Bartolomei_2008]_).

This tutorial consists of 2 parts which cover :ref:`the preparation of the working environment <prepare_environment_epileptogenicity_brainstorm>` and
:ref:`the computation of an epileptogenicty map<compute_epileptogenicity_brainstorm>`.

Scope 
-----

This tutorial illustrates the minimal steps to compute an epileptogenicity map on the HIP
and primarly consists of video demonstration backed with a brief description of the performed steps.
This tutorial should be viewed as a starter guide as it does not go into all the intricacies of epileptogenicity map computation.

For more in-depth information regarding the computation of epileptogenicity maps using Brainstorm
please refer to the following tutorial:

	* `Brainstorm's SEEG epileptogenicity maps tutorial <https://neuroimage.usc.edu/brainstorm/Tutorials/Epileptogenicity>`_

Requirements
------------

There are no techincal requirements to follow this tutorial as the needed dataset and software are available on the HIP.

HIP software used in this tutorial:

	* :doc:`Brainstorm</applications/APP_Brainstorm>` (07-Jan-2022)

HIP dataset used in this tutorial:

	* :doc:`Epimap tutorial dataset</datasets/DATASET_Epimap>` (rev1.0)
	
.. _prepare_environment_epileptogenicity_brainstorm:

Prepare the working environment
==================================

**Get the dataset**: This tutorial relies on data available in the :doc:`Epimap tutorial dataset </datasets/DATASET_Epimap>`
which can be accessed in the corresponding `publicly shared folder <https://thehip.app/apps/files/?dir=/HIP%20tutorials/Epileptogenicity%20map%20computation%20with%20Brainstorm/Datasets&fileid=682152>`_.

The following files will be used for this tutorial:

	* anat/MRI/3DT1pre_deface.nii
	* anat/MRI/3DT1post_deface.nii
	* anat/implantation/elec_pos_patient.txt
	* seeg/SZ1.TRC
	* seeg/SZ2.TRC
	* seeg/SZ3.TRC


Transfer those files into your private space so it is easier to access and use them.
If you don't know how to do this please refer to the :doc:`How to use the HIP spaces </guides/GUIDE_How_to_use_the_HIP_spaces_and_share_data_with_other_users>` guide.

**Start a new working session with Brainstorm**: This tutorial only requires the use of Brainstorm for both the placement of SEEG electrodes
and the computation of epileptogenicity maps. It is advised to initiate a new working sesssion with a fresh instance of Brainstorm running.
If you don't know how to do this please refer to the :doc:`How to use the application library and working sessions </guides/GUIDE_How_to_use_the_application_library_and_working_sessions>` guide.

.. _compute_epileptogenicity_brainstorm:

Compute a map of epileptogenicity
=================================

It is mandatory to have the 3D positions of the recording contacts of the SEEG electrodes in order to compute epileptogenicity maps. 
The contact names and coordinates of the SEEG electrodes are provided in the *elec_pos_patient.txt* implantation file that will
be used in this tutorial.
If you work on your own imaging data and wish to generate a dedicated implantation file, you can follow one of the following tutorials:

	* :doc:`SEEG electrode placement with IntrAnat [TODO] </tutorials/TUTORIAL_SEEG_electrode_placement_with_intranat>`
	* :doc:`SEEG electrode placement with Brainstorm [U/C] </tutorials/TUTORIAL_SEEG_electrode_placement_with_brainstorm>`

.. raw:: html

   <center>	
   <video width="680"  poster="https://thehip.app/apps/sharingpath/aboyer/Public/Tutorial%20-%20Epileptogenicity%20map%20computation%20with%20Brainstorm/Videos/HIP%20Tutorial%20-%20Thumbnail%20-%20Epileptogenicity%20map%20computation%20with%20Brainstorm.png" controls>
   <source src="https://thehip.app/apps/sharingpath/aboyer/Public/Tutorial%20-%20Epileptogenicity%20map%20computation%20with%20Brainstorm/Videos/HIP%20Tutorial%20-%20Epileptogenicity%20map%20computation%20with%20Brainstorm.mp4" type="video/mp4">
   Your browser does not support the video tag.
   </video>
   </center>
	
|

References
==========

.. [Bartolomei_2008] Bartolomei F, Chauvel P, Wendling F. Epileptogenicity of brain structures in human temporal lobe epilepsy: a quantified study from intracerebral EEG. Brain., 2008:131(Pt 7):1818-30.

