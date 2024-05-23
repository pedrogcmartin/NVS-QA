This directory contains the camera path information of the reference videos of each scene that is used to generate the same camera path for the synthesized videos. The COLMAP framework was used for the pose estimation of the real scenes camera paths. The camera poses of the synthetic scenes were already provided on the *Realistic Synthetic 360º* dataset and for the *Front-facing* were directly extracted from Blender using BlenderNeRF.

For the *Front-facing* and *Tanks and Temples* scenes the camera path information are processed by the camera poses and intrinsics in a separate way. Although the camera intrinsics are the same within the camera poses of each scene, for implementation purposes, two folders were created for each type of information. In each folder, each file corresponds to the respective camera information for each image to be synthesized.

For the *Realistic Synthetic 360º*  scenes the original "transforms_test.json" file of the *Realistic Synthetic 360º* dataset is used, as the selected test time interval corresponds to the images sequence contained in the original test set. Most of the implementations enabled the automatic synthesis of that test set.

# Attribute

BlenderNeRF software by M. Raafat: https://github.com/maximeraafat/BlenderNeRF