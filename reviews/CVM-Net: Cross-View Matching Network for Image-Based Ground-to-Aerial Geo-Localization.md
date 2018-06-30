## CVM-Net: Cross-View Matching Network for Image-Based Ground-to-Aerial Geo-Localization

Sixing Hu, Mengdan Feng, Rang M. H. Nguyen, Gim Hee Lee, CVPR, 2018

### Summary
1.  Propose CVM-Net for cross-view imagebased ground-to-aerial geo-localization.
2.  Contributions:
* Combine NetVLAD layers with a Siamese network to jointly learn robust representations for cross-view image matching (find the closest match of a query ground image from a given database of geo-tagged satellite images);
* Introduce a new weighted soft margin ranking loss that not only speeds up the training convergence but also improves the final retrieval accuracy.
3.  Proposed Approach:
* CNNs (AlexNet/VGG16) are used to extract the local features;
* Feed the local feature vectors into a NetVLAD layers to get the global descriptor(invariant across large viewpoint changes), where NetVLAD is a trainable deep network version of VLAD. Two strategies are tried, CVM-Net-I (Two independent NetVLADs) and CVM-Net-II (NetVLADs with shared weights);
* Use a weighted soft-margin triplet loss to train CVM-Nets.
4. Experiment:
* Dataset: 
    * [CVUSA](http://cs.uky.edu/~jacobs/datasets/cvusa/) 
    * [GT-CrossView](https://github.com/lugiavn/gt-crossview)
### Strengths / Novelties
* NetVLAD layers to encode local features into a VLAD global descriptor (which is invariant across large viewpoint changes);
![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/6.png)
