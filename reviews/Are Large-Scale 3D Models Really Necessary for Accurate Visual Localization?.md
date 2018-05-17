## Are Large-Scale 3D Models Really Necessary for Accurate Visual Localization?

Torsten Sattler, Akihiko Torii, Josef Sivic, Marc Pollefeys, Hajime Taira, Masatoshi Okutomi, Tomas Pajdla, CVPR，2017

### Summary
- Pipeline:
    * Generating Reference Poses:
        * Generating local reconstructions: generate SfM reconstructions from the database images around the query images. 
        * Geo-registration: to obtain the global positions and orientations of the cameras in each local reconstruction.
    * 2D Image-based Localization:
        * Pose Estimation for 2D-based Approaches: ①.Nearest neighbor (NN)/most relevant database image.  ②. Spatial re-ranking (SR).  ③.SfM on the fly (SfM): small-scale SfM to obtain a local 3D model around the query image.
### Strengths / Novelties
- generate reference camera pose annotations for the query images of the San Francisco Landmarks dataset.
- use this new dataset for the first comparison of 2Dand 3D-based localization approaches regarding their pose accuracy. 
- Quantitative evaluation of error.
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/1.png)
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/2.png)
