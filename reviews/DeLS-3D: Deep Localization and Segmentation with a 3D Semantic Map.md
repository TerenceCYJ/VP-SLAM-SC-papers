## DeLS-3D: Deep Localization and Segmentation with a 3D Semantic Map

Peng Wang, Ruigang Yang, Binbin Cao, Wei Xu, Yuanqing Lin, CVPR, 2018</br>
[Baidu Research](http://research.baidu.com/Research_Areas/index-view?id=58)

### Summary
1.  Contributions:
* roposed a deep learning based system for fusing multiple sensors (i.e. RGB images, customer-grad GPS/IMU );
* Jointly handle camera poses and scene semantics;
* Create a dataset which includes dense 3D semantically labelled point clouds, GT camera poses and pixel-level semantic labels of video camera images.
2.  Dataset:</br>
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/8.png)
* Data collection: </br>
>> Mobile LIDAR scanner to collect point clouds and eliminate  inaccurate moving objects;
>>Two frontal cameras with a resolution of 2048×2432 to capture video.

* 2D and 3D labeling</br>
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/9.png)
3.  Proposed Approach:
* Render a label map from a camera pose:
* Camera localization with motion prior:
    * Translation rectification with road prior, then a label map is rendered based on the rectified camera pose;
    * CNN-GRU pose network architecture:
        * CNN: inputs an image and the rendered label map (from corresponding coarse camera pose), and outputs a 7 dimension relative pose between the image and the rendered label map;
        * A multi-layer GRU with residual connection  is appended to model the temporal dependency.
    * Pose loss: use the geometric matching loss for training, which avoids the balancing factor between rotation and translation.
* Video parsing with pose guidance</br>
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/10.png)

### Strengths / Novelties：
* Using the pose after RNN, better alignment is achieved, and the segment accuracy is improved significantly；
* The two information are mutually beneficial, where pose helps give good priori for segmentation and semantic guides a better localization;
* Created a dataset which contains a point-cloud based semantic 3D map and videos with ground truth camera pose and per-frame semantic labelling.
	
### Weaknesses / Notes：
* GPS and IMU signal is very limited for training.
