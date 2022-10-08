# Medical Motion Planning Dataset (Med-MPD)

## Overview

This repository contains environments for evaluating motion planners and minimally-invasive robot designs.

## Data

### Lungs :lungs:

There are five lungs environments from the Lung Image Database Consortium and Image Database Resource Initiative ([LIDC-IDRI][1]) (CC-BY 3.0) image collection from The Cancer Imaging Archive ([TCIA][2]). We segmented the bronchial tree, pleural boundary, and major vessels using an automatic segmentation algorithm ([LINK][3]), and we segmented the nodules and lung fissures manually using [3D-Slicer][4]. 

[1]: <https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI> "LIDC-IDRI"
[2]: <https://www.cancerimagingarchive.net/> "TCIA"
[3]: <https://github.com/UNC-Robotics/lung-segmentation> "LINK"
[4]: <https://www.slicer.org/> "3D-Slicer"

### Liver

There are five liver environments from the Hepatocellular Carcinoma Transarterial Chemoembolization Segmentation ([HCC-TACE-Seg][5]) (CC-BY 4.0) image collection from The Cancer Imaging Archive ([TCIA][2]). Segmentations of the liver, cancer nodules, and blood vessels are provided as part of the data. We manually refined and expanded these segmentations using [3D-Slicer][4], as well as differentiated the vessels into the hepatic arteries, hepatic veins, and portal vein.

[5]: <https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=70230229> "HCC-TACE-Seg"

### Brain :brain:

There are five brain environments from the Healthy MR Database ([LINK][6]). We segmented the blood vessels manually using [3D-Slicer][4], and we used [FastSurfer][7] to segment the brain and all of the brain subregions.

[6]: <https://data.kitware.com/#collection/591086ee8d777f16d01e0724> "HMRD"
[7]: <https://www.sciencedirect.com/science/article/pii/S1053811920304985> "FS"

## Usage

Within each folder are segmentation files in .nii.gz format. These can easily be loaded in publicly-available software such as [3D Slicer](https://www.slicer.org/) and then converted or saved in other formats. [NiBabel](https://nipy.org/nibabel/) or [SimpleITK](https://pypi.org/project/SimpleITK/) are other convenient tools for working with these types of images. For each environment, there are text files with [RAS](https://www.slicer.org/wiki/Coordinate_systems) coordinates corresponding to the nodules and a set of 4x4 matrices for variable clinically-motivated start poses for the motion planning problem.

Inside `Utilities/` are a couple helpful functions for programmatically loading the data, converting betweeen RAS and IJK coordinates, and for visualizing the data.

We used Slicer version [4.11.20210226](https://slicer-packages.kitware.com/#collection/5f4474d0e1d8c75dfc70547e/folder/60ac0ce2ae4540bf6a899ecc).

## References

* Armato III, Samuel G., et al. "The lung image database consortium (LIDC) and image database resource initiative (IDRI): a completed reference database of lung nodules on CT scans." Medical physics 38.2 (2011): 915-931.

* Morshid, Ali, et al. "A machine learning model to predict hepatocellular carcinoma response to transcatheter arterial chemoembolization." Radiology. Artificial intelligence 1.5 (2019).

* Clark, Kenneth, et al. "The Cancer Imaging Archive (TCIA): maintaining and operating a public information repository." Journal of digital imaging 26.6 (2013): 1045-1057.

* Bullitt E, Zeng D, Gerig G, Aylward S, Joshi S, Smith JK, Lin W, Ewend MG (2005) Vessel tortuosity and brain tumor malignancy: A blinded study. Academic Radiology 12:1232-1240.

* Henschel, Leonie, et al. "Fastsurfer-a fast and accurate deep learning based neuroimaging pipeline." NeuroImage 219 (2020): 117012.

## Acknowledgements

The authors acknowledge the National Cancer Institute and the Foundation for the National Institutes of Health, and their critical role in the creation of the free publicly available LIDC/IDRI Database used in this study.

The MR brain images from healthy volunteers used in this work were collected and made available by the CASILab at The University of North Carolina at Chapel Hill and were distributed by the MIDAS Data Server at Kitware, Inc.

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License ([CC-BY-SA 4.0][6]).

Any use of this work must also abide by the [terms][7] set by the TCIA.

[6]: <http://creativecommons.org/licenses/by-sa/4.0/>
[7]: <https://wiki.cancerimagingarchive.net/display/Public/Data+Usage+Policies+and+Restrictions>


