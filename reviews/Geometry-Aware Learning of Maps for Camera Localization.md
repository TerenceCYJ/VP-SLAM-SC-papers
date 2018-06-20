## Geometry-Aware Learning of Maps for Camera Localization

S Brahmbhatt, J Gu, K Kim, J Hays, J Kautz, CVPR, 2018


### Summary

1. MapNet Proposed to represent maps as a DNN : Learns the map representation directly from input data; flexibility to fuse multiple sensory inputs and to improve over time using unlabeled data.
2. Contributions:
    * MapNet shows how the geometric constraints between pairs of observations can be included as an additional loss term in training. Constrain sources: pose constrian from VO, translation constrain from GPS, rotation constrain from IMU.
    * PoseNet et al are offline methods, the learned DNNs are fixed after training. MapNet+ can continuously update the DNN weights (i.e., maps) 
    * Proposed a new parameterization for camera rotation which is better suited for deep-learning based camera pose regression.
3. Proposed Approach:
    * Camera Pose Regression with DNNs
      * use ResNet-34 and modify PoseNet by introducing a global average pooling layer after the last conv layer, followed by a fc layer with 2048 neurons, a ReLU and dropout with p = 0:5. This is followed by a final fc layer that outputs a 6-DoF camera pose.
      * propose to parameterize camera orientation as the logarithm of a unit quaternion.
    * MapNet: Geometry-Aware Learning Data flow for our proposed algorithms. 
      * MapNet enforces geometric constraints between relative poses and absolute poses in network training. MapNet+ fuses other inputs such as visual odometry to update maps with self-supervised learning. MapNet+PGO performs PGO at testing time to further improve accuracy.
    * MapNet+: Update with Unlabeled Data
      * MapNet+ fuses additional data (IMU GPS) to update the weights of MapNet with self-supervised learning : fine-tune a pre-trained MapNet by minimizing a loss function that consists of the original loss from the labelled dataset D and the loss from the unlabeled data T .
    * MapNet+PGO: Optimizing During Inference
	MapNet+PGO fuses the absolute pose predictions from MapNet+ and the relative poses from VO using pose graph optimization (PGO) to get
smooth and globally consistent pose predictions. 
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/5.png)
### Strengths / Novelties
MapNet+ use unlabeled videos and multiple sensory input.
