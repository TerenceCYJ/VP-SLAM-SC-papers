## Learning to Localize Sound Source in Visual Scenes

Arda Senocak, Tae-Hyun Oh, Junsik Kim, Ming-Hsuan Yang, In So Kweon, CVPR, 2018

### Keywords：
sound source localization; cross-modal supervised network; attention model

### Summary
1.  Contributions:
* Introduce a learning framework to localize sound source using the attention mechanism, which is guided by sound information, with a paired sound and video frame;
* Propose a unified end-to-end deep convolutional neural network architecture that accommodates unsupervised, semi-supervised, and fully-supervised learning;
* Collect and annotate a new sound source localization dataset, which provides supervised information and facilitates quantitative and qualitative analysis.
2.  Proposed Approach:
* Design a neural network to address the problem of vision based sound localization within the unsupervised learning framework;
* The network composes of three main modules: sound network, visual network and attention model.
    * Sound Network: The input is a 1-D signal with varying temporal length, the output is 512-D.
    * Visual Network: Composed of the image feature extractor and localization module.
       * Image feature extractor: 512-D activation vector contains local visual context information.
       * Localization module returns a confidence map of sound source and a representative visual feature vector z corresponding to location of source of the given input sound.
    * Localization Network: Given extracted visual and sound concepts, the localization networks generate the sound source location.
* Localizing Sound Source via Listening.
3.  Dataset:
* Leverage the large unlabeled FlickrSoundNet dataset;
* Provides annotations for training supervision models.
>>![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/11.png)

>>![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/12.png)
</br>


### Strengths / Novelties：
* By empirically demonstrating the capability of our unsupervised network, we show the model plausibly works in a variety of categories but partially, in that, without prior knowledge, the network can often get to false conclusion.
* Leveraging small amount of human knowledge can discipline the model, so that it can correct to capture semantically meaningful relationships.
* Deduce the way of machine understanding about sound source localization in visual scenes.
* Potential directions for future research, i.e., multi-modal retrieval, sound based saliency or representation learning and its applications.
