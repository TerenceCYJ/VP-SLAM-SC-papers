## Benchmarking 6DOF Outdoor Visual Localization in Changing Conditions

Torsten Sattler, Will Maddern, Carl Toft, Akihiko Torii, Lars Hammarstrand, Erik Stenborg, Daniel Safari, Masatoshi Okutomi, Marc Pollefeys, Josef Sivic, Fredrik Kahl, Tomas Pajdla, CVPR, 2018

### Summary
1.  Contributions:
* Construct the first datasets for benchmarking visual localization under changing conditions;
* Provide an extensive experimental evaluation of state-of-the-art algorithms;
* We show the value of querying with multiple images, rather than with individual photos, especially under challenging conditions;
2.  Data Preparation:
* The Aachen Day-Night Dataset:
>>Use COLMAP to create an intermediate 3D model from the reference and query images to obtain ground truth poses；Night-time queries:Using the resulting 2D-3D matches and the known intrinsics of the camera, we estimate the camera poses using a 3-point solver and non-linear pose refinement.
* The RobotCar Seasons Dataset:
>>Used the LIDAR scanners mounted to the vehicle to build local 3D point clouds, and models were then aligned to the LIDAR point clouds of the reference trajectory using ICP，and the alignments provided ground truth poses for the query images.
* The CMU Seasons Dataset:
>>Based on a subset of the CMU Visual Localization Dataset.
		
3.  Proposed Approach:
* Evaluation measures：
>>Position error: Euclidean distance;
>>Orientation error: an angle in degrees;
* Evaluated algorithms:
>>3D structure-based methods: Active Search(AS) and City-Scale Localization (CSL);
>>2D image retrieval-based approaches: DenseVLAD, NetVLAD, and FAB-MAP.
		
4. Others:
* Comparison of localization benchmarks
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/7.png)

### Strengths / Novelties：
* Introduced three challenging new benchmark datasets for visual localization.

### Weaknesses / Notes：
* Long-term visual localization problem is far from solved;
* Due to limitations of existing local features:
    * **Dense CNN feature**:improves pose estimation performance at high computational costs, but does not fully solve the problem;
    * **Novel (dense) features** are required;
    * **Image-level descriptors**: Aiming to improve pose accuracy,e.g., by denser view sampling via synthetic images or image-level approaches for relative pose estimation, is an interesting research direction;
* There is a clear benefit in using **multiple images for pose estimation**. Yet, there is little existing work on multi-image localization.
