## PoseNet: A Convolutional Network for Real-Time 6-DOF Camera Relocalization

Alex Kendall， Matthew Grimes，Roberto Cipolla， University of Cambridge， ICCV， 2015


### Summary
- Relocalize
    * ~ 2m and 3° accuracy for large outdoor scene (spanning 50,000㎡);<br>
      0.5m and 5° accuracy indoors;<br>
      5ms - 95ms to run with GPU;<br>
      Input: 224*224 RGB image; <br>
      Output:camera's 6-DoF pose relative to scene.<br>
- DCNN camera pose regressor:
    * Leverage transfer learning from recognition to relocalization.
    * Use SfM to generate training labels(camera pose) from video of the scene.
    * Training: 
        * Train the convnet on Euclidean Loss using SGD.
        * Basis of network: GoogLeNet.
        * Modified GoogLeNet as follows:
          * Replace all three softmax classifiers with affine regressors;<br>
          * Insert another fully connected layer before the final regressor of feature size 2048;<br>
          * At test time, normalize the quaternion orientation vector to unit length.<br>
 
        * baselearning rate 10-5,  reduced by 90% every 80 epochs and with momentum of 0.9,  batch size of 75.
        * Dataset:
          * Release  an outdoor urban localization dataset [Cambridge Landmarks](http://mi.eng.cam.ac.uk/projects/relocalisation/) with 5 scenes;
          * Test on indoor scenes using [RGB-D 7 Scenes dataset](https://www.microsoft.com/en-us/research/project/rgb-d-dataset-7-scenes/).
- Understanding the representation that convnet generates:
    * the system learns to compute feature vectors which are easily mapped to pose;
    * the strongest response is observed from higher-level features such as windows andspires;
    * sensitive to large textureless patches such as road, grass and sky.
### Strengths / Novelties
- the first application of deep convolutional neural networks to end-to-end 6-DOF camera pose localization;
- Tolerates large baselines that cause SIFT-based localizers to fail sharply.

### Weaknesses / Notes
- Data-hungery === lots of image to present a scene.
- Pursue further uses of multiview geometry as a source of training data for deep pose regressors.
