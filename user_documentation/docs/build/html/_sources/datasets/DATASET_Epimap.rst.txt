Epimap tutorial dataset
**********************************

Description
===========

This dataset includes recordings for a patient that was not reported in associated articles ([David_2011]_, [Lamarche_2016]_),
but is part of the same study. The patient presents a focal epilepsy of the left temporo-occipital junction, MRI-negative,
and was implanted in the surrounding areas.
The subfolder "seeg" contains the recordings of three seizures, all of them showing a propagation of high-frequency oscillations
from the lesion towards the temporal lobe, bilaterally.

Data files
-----------

The dataset is accessible in a `publicly shared folder <https://thehip.app/apps/files/?dir=/HIP%20tutorials/Epileptogenicity%20map%20computation%20with%20Brainstorm/Datasets&fileid=682152>`_
and includes the following files:

	* anat/MRI/3DT1\*_deface.nii: Subject T1 MRI before and after SEEG implantation, de-identified with FreeSurfer's mri_deface
	* anat/MRI/brainvisa: Cortical surface extracted with BrainVISA 4.5
	* anat/implantation/\*.txt: Positions of the sEEG contacts in various formats (MNI coordinates or subjecy coordinates)
	* seeg/SZ*.TRC: Seizure recordings in Micromed format, one seizure per file
	
It can also be downloaded from the original publisher on `f-tract.eu <https://f-tract.eu/ImaGIN_datasets/tutorial_epimap>`_.

	
Electrode description
---------------------

The depth electrodes used in this example dataset are DIXI D08-\**AM Microdeep electrodes, with the following specifications:

	* Diameter: 0.8 mm
	* Contact length: 2 mm
	* Insulator length: 1.5 mm
	* Distance between the center of two contacts: 3.5 mm
	* Between 8 and 18 contacts on each electrode
	

License
=======

This tutorial dataset (EEG and MRI data) is the property of the Grenoble University Hospital, France.
Its use and transfer outside the ImaGIN tutorial, e.g. for research purposes, is prohibited without written consent.
For questions, please contact Olivier David, PhD (olivier.david@univ-grenoble-alpes.fr).

References
==========

The acquisition methodology is described in the following articles :

.. [David_2011] David O, Blauwblomme T, Job AS, Chabardès S, Hoffmann D, Minotti L, Kahane P. "Imaging the seizure onset zone with stereo-electroencephalography Brain." Brain., 2011: 134(10):2898-911.

.. [Lamarche_2016] Lamarche F, Job AS, Deman P, Bhattacharjee M, Hoffmann D, Gallazzini-Crépin C, Bouvard S, Minotti L, Kahane P, David O. "Correlation of FDG-PET hypometabolism and SEEG epileptogenicity mapping in patients with drug-resistant focal epilepsy Epilepsia." Epilepsia., 2016: 57(12):2045–2055.



