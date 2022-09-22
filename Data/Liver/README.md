# Overview

Within each folder are segmentation files in .nii.gz format. These can easily be loaded in publicly-available software such as [3D Slicer](https://www.slicer.org/) and then converted/saved in other formats. [NiBabel](https://nipy.org/nibabel/) is another convenient tool for handing with different image formats and representations. There are segmentations of the liver, hepatic arteries, hepatic veins, portal vein, and nodules. In addition, there are text files with RAS coordinates for the nodules and a set of 4x4 matrices for variable clinically-motivated start poses for the motion planning problem.

Inside `Utilities/` are a couple helpful scripts for visualizing the data.

The corresponding patient identifier in the LIDC-IDRI dataset for each patient is:
* Patient1 - HCC_001
* Patient2 - HCC_031
* Patient3 - HCC_057 (environment used in paper figure)
* Patient4 - HCC_079
* Patient5 - HCC_094 
