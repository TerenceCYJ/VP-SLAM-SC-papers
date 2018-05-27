## Deep Image Retrieval: Learning global representations for image search

Albert Gordo, Jon Almazán, Jerome Revaud, and Diane Larlus, CVPR 2016.


### Summary
1. Build a deep representation for retrieval: Regional Maximum activations of Convolutions (R-MAC).
    * leverage a three-stream Siamese network with a triplet ranking loss;
    * learn the pooling mechanism using a region proposal network (RPN) instead of relying on a rigid grid;
    * building a global descriptor：use network to represent a high-solution image;
2. Learning the pooling mechanism of the R-MAC descriptor:  to predict the location of these regions given the image content.
3. Leveraging large-scale noisy data
    * Cleaning the Landmarks dataset: 
      * non-negligible amount of unrelated images;
      * run a strong image matching baseline within the images of each landmark class:  SIFT and Hessian-Affine keypoint detectors and match keypoints using the first-to-second neighbor ratio rule, verify all matches with an affine transformation model;
      * only retain the largest connected component and discard the rest;
    * Bounding box estimation: a learned ROI selector.

4. Experiments
    * Datasets: Oxford 5k、Paris 6k、Oxford 105k、Paris 106k、Holidays dataset
    * Net： VGG16 pre-trained on ImageNet ILSVRC challenge


### Strengths / Novelties
1.   Siamese architecture trained with a ranking  ——> loss deeply train our network for the specific task of image retrieval.
2.   region proposal networks ——> demonstrate the benefit of predicting and pooling the likely locations of regions of interest when encoding the images.

![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/4.png)
