## InLoc: Indoor Visual Localization with Dense Matching and View Synthesis

Hajime Taira, Masatoshi Okutomi, Torsten Sattler, Mircea Cimpoi, Marc Pollefeys, Josef Sivic, Tomas Pajdla, Akihiko Torii, CVPR, 2018

### Keywords:
pose verification with view synthesis; image retrieval based localization; coarse-to-fine manner; dense matching

### Summary
#### 1.  Contributions:
* Develop a new large-scale visual localization method targeted for indoor environments:
    * Introducing dense feature extraction and matching in a sequence of progressively stricter verification steps;
    * The first to clearly demonstrate the benefit of dense association for indoor localization.

* Collect a new dataset with reference 6DoF poses for large-scale indoor localization, and the dataset contains large variation in appearance between queries and the 3D database.
#### 2.  Dataset：
* InLoc dataset：
    * Captured from smartphone.
    * Capture the variety of occluders and layouts (e.g., people, furniture) as well as illumination changes.
* Two properties:
    * large-scale.
    * Use mobile phone to capture images at a time months apart from the date of capture of the reference 3D model (changes in scene appearance of images and 3D model).
* Scanned sparsely on purpose to cover a larger area with a small number of scans. Leads to critical view changes between query and database images.
#### 3.  Proposed Approach:
* Three main challenges of indoor environment:
    * Lack of sparse local features --> use multi-scale dense CNN features for both image description and feature matching;
    * Large image changes --> dense feature matches to collect as much positive evidence as possible;
    * Self-similarity --> compare the query image with a virtual view of the 3D model rendered from the estimated camera pose of the query.
* Pipeline of InLoc:
    *  Candidate pose retrieval:
	    *  Images are described by NetVLAD;
	    *  Compute the normalized L2 distances of the descriptors.
    * Pose estimation using dense CNN matching:
	    *  Use an image representation extracted by a VGG-16 as a set of multi-scale features extracted on a regular grid that describes more higher-level information with a larger receptive field.
	    *  The query camera pose can be estimated by finding pixel-to-pixel correspondences between the query and the matching database image followed by P3P-RANSAC.
    * Re-rank the computed camera poses based on verification by view synthesis.
	    *  Achieved by harnessing the power of the high-quality RGBD image database that provides a dense and accurate 3D structure of the indoor environment.
	    *  By counting which regions are and are not consistent between the query image and the underlying 3D structure.
>>![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/13.png)
#### 4.  Experiment:
* Retrieval 100 candidate database images using NetVLAD, and Pitts30K pre-trained VGG-16 to generate 4096D NetVLAD descriptor vectors;
* A coarse-to fine manner: Find matches in the finer conv3 features restricted by the coarse conv5 correspondences. Re-rank the 100 candidates using the number of RANSAC inliers and keep the top-10 databaseimages, and compute the 6DoF pose for 10 images by P3P-LO-RANSAC.
* Generate synthesized cviews --> Use DenseSIFT extractor and its RootSIFT descriptor to measure the similarity --> localize the query image by the best pose.

		
### Strengths / Novelties：
* Standard geometric verification based on local feature detection does not work on textureless or self-repetitive scenes, this paper use features densely extracted on a regular grid for verifying and re-ranking the candidate images by feature matching and pose estimation.
* Pose estimation using dense matching;
* Pose verification to the top-10 pose estimates with view synthesis;
* A binary representation (instead of floats) of features in the intermediate CNN layers significantly reduces memory requirements.


