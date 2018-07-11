## Papers Recommended by VALSE2018 Talk 《2017以来的2D to 3D》
---
### 1. Image Matching
#### 1.1 Learning-based Feature Detection Algorithm
  * CovDet
  * AffNet
#### 1.2 Learning-based Feature Descriptor
  * L2Net
  * DeepCD
  * Spread-out
  * HardNet
#### 1.3 Feature Matching Method
  * GMS
  * SGM-Nets
#### 1.4 Descriptor Evaluation
  * Comparative Evaluation of Hand-Crafted and Learned Local Features
  * A benchmark and evaluation of handcrafted and learned local descriptor.

---
### 2. Visual Localization
#### 2.1 3D Points are Known
##### 2.1.1 Overview
  - Are Large-scale 3D Models Really Necessary for Accurate Visual Localization?
    - 1
  - A survey on Visual-Based Localization: On the benefit of heterogeneous data
    - 1

##### 2.1.2 Large-scale & Heterogeneous Data
  - Efficient Global 2D-3D Matching for Camera Localization in Large-Scale 3D Map
    - 1
  - Globally-Optimal Inlier Set Maximisation for Simultaneous Camera Pose and Feature Correspondence  [[Paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Campbell_Globally-Optimal_Inlier_Set_ICCV_2017_paper.pdf)] [[Video](https://www.youtube.com/watch?v=DCG9PXEzyPU&t=13s)]
    - Dylan Campbell, Lars Petersson, Laurent Kneip, Hongdong Li, ICCV, 2017 
  - Real-time SLAM relocalization with online learning of binary feature indexing
  [[Paper](https://link.springer.com/article/10.1007/s00138-017-0873-z)]
    - Youji Feng, Yihong Wu, Lixin Fan, Machine Vision and Applications, 2017
  - Delving Deeper into Convolutional Neural Networks for Camera Relocalization
  [[Paper](http://xlhu.cn/papers/Wu17-icra.pdf)]
    - Jian Wu, Liwei Ma, Xiaolin Hu, ICRA, 2017
  - Relocalization, Global Optimization and Map Merging for Monocular Visual-Inertial SLAM
  [[Paper](https://arxiv.org/pdf/1803.01549)]
  - Tong Qin, Perliang Li, Shaojie Shen, ICRA, 2018
  

#### 2.2 3D Points are Unknown
##### 2.2.1 Overview
  - Image Based Camera Localization: an Overview.
  - Past, Present, and Future of Simultaneous Localization and Mapping: Toward the Robust-Perception Age
  [[Paper](https://ieeexplore.ieee.org/abstract/document/7747236/)]
    - Cesar Cadena, Luca Carlone, Henry Carrillo, Yasir Latif, Davide Scaramuzza, Jose Neira, Ian Reid, John J. Leonard, IEEE Transactions on Robotics, 2016
  - Keyframe-based monocular SLAM: design, survey, and future directions
  [[Paper](https://www.sciencedirect.com/science/article/pii/S0921889017300647)]
    - Georges Younes, Daniel Asmar, Elie Shammas, John Zelekb, Robotics and Autonomous Systems, 2017
##### 2.2.2 Robust Visual Localization in Complex Environments
  - PL-SLAM: Real-time monocular visual SLAM with points and lines 
  [[Paper](https://arxiv.org/pdf/1705.09479)]
    - Ruben Gomez-Ojeda, David Zuñiga-Noël, Francisco-Angel Moreno, Davide Scaramuzza, Javier Gonzalez-Jimenez, ICRA, 2017
  - Direct Monocular Odometry Using Points and Lines
  [[Paper](https://arxiv.org/pdf/1703.06380)]
    - Shichao Yang, Sebastian Scherer, ICRA, 2017
  - Pop-up SLAM: Semantic Monocular Plane SLAM for Low-texture Environments [[Paper](https://arxiv.org/pdf/1703.07334)]
    - Shichao Yang, Yu Song, Michael Kaess, Sebastian Scherer, IROS, 2016
  - Probabilistic RGB-D odometry based on points, lines and planes under depth uncertainty [[Paper](https://www.sciencedirect.com/science/article/pii/S0921889017303378)]
    - Pedro F.Proença, Yang Gao, Robotics and Autonomous Systems, 2018
  - Robust Stereo Visual Inertial Odometry for Fast Autonomous Flight [[Paper](https://ieeexplore.ieee.org/abstract/document/8258858/)]
    - Ke Sun, Kartik Mohta, Bernd Pfrommer, IEEE Robotics and Automation Letters, 2018
  - Stereo DSO: Large-Scale Direct Sparse Visual Odometry with Stereo Cameras [[Paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Wang_Stereo_DSO_Large-Scale_ICCV_2017_paper.pdf)]
    - Rui Wang, Martin Schworer, Daniel Cremers, ICCV, 2017
  - Model-Based Global Localization for Aerial Robots Using Edge Alignment [[Paper](https://ieeexplore.ieee.org/abstract/document/7835174/)]
    - Kejie Qiu, Tianbo Liu, Shaojie Shen, IEEE Robotics and Automation Letters, 2017
  - Edge alignment-based visual–inertial fusion for tracking of aggressive motions [[Paper](https://link.springer.com/article/10.1007/s10514-017-9642-0)]
    - Yonggen Ling, Manohar Kuse, Shaojie Shen, Autonomous Robots, 2017
  - Building maps for autonomous navigation using sparse visual SLAM features
  [[Paper](https://ieeexplore.ieee.org/abstract/document/8202316/authors)]
    - Yonggen Ling, Shaojie Shen, IROS, 2017
##### 2.2.3 Visual Localization fused with Deep learning or Geometry
  - CNN-SLAM: Real-time dense monocular SLAM with learned depth prediction
  [[Paper](http://openaccess.thecvf.com/content_cvpr_2017/papers/Tateno_CNN-SLAM_Real-Time_Dense_CVPR_2017_paper.pdf)]
    - Keisuke Tateno, Federico Tombari, Iro Laina, Nassir Navab, CVPR, 2017
  - DeMoN: Depth and Motion Network for Learning Monocular Stereo [[Paper](http://openaccess.thecvf.com/content_cvpr_2017/papers/Ummenhofer_DeMoN_Depth_and_CVPR_2017_paper.pdf)]
    - Benjamin Ummenhofer, Huizhong Zhou, Jonas Uhrig, Nikolaus Mayer, Eddy Ilg, Alexey Dosovitskiy, Thomas Brox, CVPR, 2017
  - Unsupervised Learning of Depth and Ego-Motion from Video [[Paper](http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhou_Unsupervised_Learning_of_CVPR_2017_paper.pdf)]
    - Tinghui Zhou, Matthew Brown, Noah Snavely, David G. Lowe, CVPR, 2017
  - SfM-Net: Learning of Structure and Motion from Video [[Paper](https://arxiv.org/abs/1704.07804)]
    - Sudheendra Vijayanarasimhan, Susanna Ricco, Cordelia Schmid, Rahul Sukthankar, Katerina Fragkiadaki, arXiv, 2017
  - UnDeepVO: Monocular Visual Odometry through Unsupervised Deep Learning [[Paper](https://arxiv.org/abs/1709.06841)]
    - Ruihao Li, Sen Wang, Zhiqiang Long, Dongbing Gu, arXiv, 2017
  - Toward Geometric Deep SLAM [[Paper](https://arxiv.org/abs/1707.07410)]
    - Daniel DeTone, Tomasz Malisiewicz, Andrew Rabinovich, arVix, 2017
  - Unsupervised learning to detect loops using deep neural networks for visual SLAM system [[Paper](https://link.springer.com/article/10.1007/s10514-015-9516-2)]
    - Xiang Gao, Tao Zhang, Autonomous Robots, 2017
  - Deep EndoVO: A recurrent convolutional neural network (RCNN) based visual odometry approach for endoscopic capsule robots [[Paper](https://ac.els-cdn.com/S092523121731665X/1-s2.0-S092523121731665X-main.pdf?_tid=f2f2f18d-3c2d-46b4-af5d-1654d4abbe02&acdnat=1531310665_66e84713009c6658695b54c7343f1f9a)]
    - Mehmet Turan, Yasin Almalioglu, Helder Araujo, Ender Konukoglu, Metin Sitti, Neurocomputing, 2018
##### 2.2.4 Semantic SLAM
  - Probabilistic data association for semantic SLAM [[Paper](https://www.researchgate.net/publication/318697576_Probabilistic_data_association_for_semantic_SLAM)]
    - Sean L. Bowman, Nikolay Atanasov, Kostas Daniilidis,George J. Pappas, ICRA, 2017
  - SemanticFusion: Dense 3D Semantic Mapping with Convolutional Neural Networks [[Paper](https://www.researchgate.net/publication/308262833_SemanticFusion_Dense_3D_Semantic_Mapping_with_Convolutional_Neural_Networks)]
    - John McCormac, Ankur Handa, Andrew Davison, Stefan Leutenegger, ICRA, 2017
##### 2.2.5 SLAM based on Marker
  - ChromaTag: A Colored Marker and Fast Detection Algorithm [[Paper](https://www.computer.org/csdl/proceedings/iccv/2017/1032/00/1032b481-abs.html)]
    - Joseph DeGol, Timothy Bretl, Derek Hoiem
  - Mapping and Localization from Planar Markers [[Paper](https://www.researchgate.net/publication/303749967_Mapping_and_Localization_from_Planar_Markers)]
##### 2.2.5 Event camera SLAM, RGBD SLAM
  - Event-based, 6-DOF Camera Tracking from Photometric Depth Maps [[Paper](https://www.researchgate.net/publication/320847681_Event-based_6-DOF_Camera_Tracking_from_Photometric_Depth_Maps)]
    - Guillermo Gallego, Jon E.A. Lund, Elias Mueggler, IEEE Transactions on Pattern Analysis and Machine Intelligence, 2017
  - Ultimate SLAM? Combining Events, Images, and IMU for Robust Visual SLAM in HDR and High-Speed Scenarios [[Paper](https://ieeexplore.ieee.org/abstract/document/8258997/)]
    - Antoni Rosinol Vidal, Henri Rebecq, Timo Horstschaefer, IEEE Robotics and Automation Letters, 2018
  - Real-time Visual-Inertial Odometry for Event Cameras using Keyframe-based Nonlinear Optimization [[Paper](https://www.semanticscholar.org/paper/Real-time-Visual-Inertial-Odometry-for-Event-using-Rebecq/0836d9e19966e00080d3b3f56d70667cc6cefd68)]
    - Henri Rebecq, BMVC, 2017

### 3. 3D Reconstruction
#### 3.1 SfM
##### 3.1.1 Overview
  - A Survey on Structure from Motion [[Paper](http://pdfs.semanticscholar.org/6562/880ada35f0410ad6c4db941586bb2b0ebdb1.pdf)]
    - O Ozyesil,  V Voroninski, R Basri, A Singer, Acta Numerica, 2017
##### 3.1.2 Incremental (增量式)
  - Batched Incremental Structure-from-Motion [[Paper](https://ieeexplore.ieee.org/abstract/document/8374573/)]
    - Hainan Cui, Shuhan Shen, Xiang Gao, Zhanyi Hu, 3DV, 2017
  - Elaborate Scene Reconstruction with a Consumer Depth Camera [[Paper](https://link.springer.com/article/10.1007/s11633-018-1114-2)]
    - Jian-Wei Li, Wei Gao, Yi-Hong Wu, International Journal of Automation and Computing, 2018
##### 3.1.3 Global (全局式)
  - Global Fusion of Generalized Camera Model for Efficient Large-Scale Structure from Motion [[Paper](http://scis.scichina.com/en/2017/038101.pdf)]
  - Hainan CUI, Shuhan SHEN, Zhanyi HU, Science China Information Sciences, 2017
##### 3.1.4 Hybrid（混合式)
  - HSfM: Hybrid Structure-from-Motion [[Paper](http://openaccess.thecvf.com/content_cvpr_2017/papers/Cui_HSfM_Hybrid_Structure-from-Motion_CVPR_2017_paper.pdf)]
    - Hainan Cui, Xiang Gao, Shuhan Shen, Zhanyi Hu, CVPR, 2017
  - CSFM: Community-based structure from motion [[Paper](https://ieeexplore.ieee.org/abstract/document/8297137/authors)]
    -  Hainan Cui,  Shuhan Shen,  Xiang Gao,  Zhanyi Hu, ICIP, 2017
  - Parallel Structure from Motion from Local Increment to Global Averaging [[Paper](https://arxiv.org/abs/1702.08601)]
    - Siyu Zhu, Tianwei Shen, Lei Zhou, Runze Zhang, Jinglu Wang, Tian Fang, Long Quan, ICCV, 2017

##### 3.1.5 Bundle Adjustment
  - Distributed very large scale bundle adjustment by global camera consensus [[Paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Zhang_Distributed_Very_Large_ICCV_2017_paper.pdf)]
    - ICCV, 2017
  - Accurate and efficient ground-to-aerial model alignment [[Paper](https://www.sciencedirect.com/science/article/pii/S0031320317304570)]
  - Gao Xiang, Hu Lihua, Cui Hainan, Shen Shuhana, Hu Zhanyi, Pattern Recognition, 2018
##### 3.1.6 Ground-to-Aerial Model Alignment
  - Accurate and efficient ground-to-aerial model alignment [[Paper](https://www.sciencedirect.com/science/article/pii/S0031320317304570)]
    - Gao Xiang, Hu Lihua, Cui Hainan, Shen Shuhan, Hu Zhanyi, Pattern Recognition, 2018
  - Accurate mesh-based alignment for ground and aerial multi-view stereo models [[Paper](https://ieeexplore.ieee.org/abstract/document/8296758/)]
    - Yang Zhou, Shuhan Shen, Xiang Gao, Zhanyi Hu, ICIP, 2017
  - Distributed Very Large Scale Bundle Adjustment by Global Camera Consensus [[Paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Zhang_Distributed_Very_Large_ICCV_2017_paper.pdf)]
    - Runze Zhang, Siyu Zhu, Tian Fang, Long Quan, ICCV, 2017
























 













 




