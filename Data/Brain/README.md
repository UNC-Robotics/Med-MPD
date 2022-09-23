# Overview

The corresponding patient identifier in the Healthy MR Database for each patient is:
* Patient1 - Normal_001
* Patient2 - Normal_003 (environment used in paper figure)
* Patient3 - Normal_005
* Patient4 - Normal_027
* Patient5 - Normal_035

There seems to be some issue in Slicer that does not allow for the full segmentation of the blood vessels to be saved after an Elastix transformation has been applied to it. Therefore, the vessels segmentations are in the coordinates of a different image than all the other segmentations. To adjust this, we need to use the original MRA file and T1 file from Healthy MR Database ([LINK](https://data.kitware.com/#collection/591086ee8d777f16d01e0724)) and perform the Elastix registration in 3D Slicer ([LINK](https://lassoan.github.io/SlicerSegmentationRecipes/VesselSegmentationBySubtraction/)). We are working on resolving this so that all segmentations are in the same image space.
