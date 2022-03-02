Epileptogenicity map computation with Brainstorm
***********************************************************

.. figure:: /art/tutorial_epileptogenicity_header.png
	:width: 600px
	:align: center

	**Epileptogenicity map.** *Epileptogenicity map computed and visualized using Brainstorm.*

Disclaimer
==========

The methods and softwares used in this tutorial have not been certified for clinical practice and should be considered for 
research purposes only.  

About this tutorial
====================

Objective
---------

The objective of this tutorial is to guide HIP users in computing maps of epileptogenicity from ictal iEEG recordings.

Epileptogenicity maps show the spatial distribution of the Epileptogenicity Index in the subject's brain.
The Epileptogenicity Index, is based on both spectral and temporal properties of iEEG signals
and quantifies the presence of high-frequency oscillations also referred as rapid discharges.
Rapid discharges have long been recognized as a characteristic electrophysiological pattern of the epileptogenic zone
and can help identify brain regions generating seizures ([Bartolomei_2008]_).

This tutorial consists of 3 parts which cover :ref:`the preparation of the working environnement <prepare_environment>`,
:ref:`the placement of SEEG electrodes<place_seeg_electrodes>` 
and finally :ref:`the computation of an epileptogenicty map<compute_epileptogenicity_map>`.

Scope 
-----

This tutorial illustrate the minimal steps to compute an epileptogenicity map on the HIP
and consists of video demonstrations backed with a brief description of the performed steps. 

This tutorial should be viewed as a starter guide as it does not go into all intricacies of epileptogenicity map computation.

For more in-depth information regarding the computation of epileptogenicity maps using Brainstorm
please refer to the following tutorials:

	* `Brainstorm's electrode placement tutorial <https://neuroimage.usc.edu/brainstorm/Tutorials/Epileptogenicity#Editing_implantation_without_recordings>`_   
	* `Brainstorm's SEEG epileptogenicity maps tutorial <https://neuroimage.usc.edu/brainstorm/Tutorials/Epileptogenicity>`_

Requirements
------------

There are no techincal requirements to follow this tutorial as the needed dataset and software are available on the HIP.

HIP software used in this tutorial:

	* :doc:`APP - Brainstorm</applications/APP_Brainstorm>` (07-Jan-2022)

HIP dataset used in this tutorial:

	* :doc:`DATASET - Epimap tutorial dataset</datasets/DATASET_Epimap>` (rev1.0)
	

.. _prepare_environment:

Prepare the working environment
==================================

**Get the dataset**: This tutorial relies on data available in the :doc:`Epimap tutorial dataset </datasets/DATASET_Epimap>`
which can be accessed in the corresponding `publicly shared folder <https://thehip.app/apps/files/?dir=/HIP%20tutorials/Epileptogenicity%20map%20computation%20with%20Brainstorm/Datasets&fileid=682152>`_.
Transfer the whole dataset into your private space so you can easily access and modify it.
If you don't know how to do this please refer to the :doc:`How to use the HIP spaces </guides/GUIDE_How_to_use_the_HIP_spaces_and_share_data_with_other_users>` guide.

**Start a new working session with Brainstorm**: This tutorial only requires the use of Brainstorm for both the placement of SEEG electrodes
and the computation of epileptogenicity maps. It is advised to initiate a new working sesssion with a fresh instance of Brainstorm running.
If you don't know how to do this please refer to the :doc:`How to use the application library and working sessions </guides/GUIDE_How_to_use_the_application_library_and_working_sessions>` guide.

.. _place_seeg_electrodes:

Place SEEG electrodes
=====================

The following files will be used in this section:

	* anat/MRI/3DT1post_deface.nii

The accurate placement of SEEG electores requires knowledge and understanding of the implantation procedure (implantation scheme or equivalent),
of the type of material that has been implanted (SEEG electrode type), and some expertise in brain anatomy. 
It is also important to work on a post-implantation high-resolution CT scan or T1 MRI scan which will show SEEG contacts in hypersignal
or hyposignal respectively.

For confidentiality reasons, the implantation scheme will not be disclosed and the video demonstration only shows the technical
procedure in order to place SEEG electrodes and generate an implantation file using Brainstorm.


.. raw:: html

   <center>	
   <video width="680"  poster="https://thehip.app/apps/sharingpath/aboyer/Public/Tutorial%20-%20SEEG%20electrode%20placement%20with%20Brainstorm/Videos/HIP%20Tutorial%20-%20Thumbnail%20-%20SEEG%20electrode%20placement%20with%20Brainstorm.png" controls>
   <source src="https://thehip.app/apps/sharingpath/aboyer/Public/Tutorial%20-%20SEEG%20electrode%20placement%20with%20Brainstorm/Videos/HIP%20Tutorial%20-%20SEEG%20electrode%20placement%20with%20Brainstorm.mp4" type="video/mp4">
   Your browser does not support the video tag.
   </video>
   </center>

|

.. _compute_epileptogenicity_map:

Compute a map of epileptogenicity
=================================

The following files will be used in this section:

	* anat/MRI/3DT1pre_deface.nii
	* anat/MRI/3DT1post_deface.nii
	* anat/implantation/elec_pos_patient.txt
	* seeg/SZ1.TRC
	* seeg/SZ2.TRC
	* seeg/SZ3.TRC
	
It is mandatory to have the 3D positions of the recording contacts of the SEEG electrodes in order to compute epileptogenicity maps. 
The conctact coordinates of the SEEG electrodes are compiled in an implantation file "elec_pos_patient.txt" that will be used in this tutorial.


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

.. [Bartolomei_2008] Bartolomei F, Chauvel P, Wendling F. Epileptogenicity of brain structures in human temporal lobe epilepsy: a quantified study from intracerebral EEG." Brain., 2008:131(Pt 7):1818-30.

