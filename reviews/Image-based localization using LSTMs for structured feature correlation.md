## Image-based localization using LSTMs for structured feature correlation

F. Walch， C. Hazirbas， L. Leal-Taixé， T. Sattler， S. Hilsenbeck， D. Cremers ，ICCV, 2017.


### Summary

1. propose a new CNN+LSTM architecture for camera pose regression in indoor and outdoor scenes.
    * CNN architecture: feature extraction
      * Leverage Places pretrained GoogLeNet
      * Loss function the same as PoseNet
    * Structured feature correlation with LSTMs


2. Extensive quantitative comparison of CNN-based and SIFT-based localization methods:  <br>
    * classic SIFT-based methods still outperform all CNN-based methods.<br>
    * CNN-based method can handle such a challenging scenario while SIFT-based methods fail completely.

3. A new challenging large indoor dataset TUM-LSI: <br>
    * exhibiting repetitive structures and weakly textured surfaces, and provide accurate ground truth poses.
    
### Strengths / Novelties
1. LSTM-based structured feature correlation can lead to drastic improvements in localization performance compared to other CNN-based methods.
2. Succeeds in a very challenging scenario where SIFT-based methods fail.
3. Exploring CNN-based localization in hard scenarios is a promising research direction.
 <br> <br> <br>
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/3.png)
