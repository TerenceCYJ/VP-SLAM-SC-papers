## Finding beans in burgers: Deep semantic-visual embedding with localization
 Authors: Martin Engilberge, Louis Chevallier, Patrick P´ erez, Matthieu Cord, CVPR, 2018

 Keywords: Visual-semantic embedding, object localization

### Contributions
*  Achieves high performance on cross-modal retrieval tasks as well as on phrases localization.
    
### Proposed Approach
* Semantic-Visual embedding
    * DCNN(ResNet) for images and simple recurrent unit network to encode the textual information. Fine-tuning and triplet-based optimization in learning scheme；
    * Generating a joint embedding space that offers rich descriptors for both images and texts；
>>![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/15.png)
*  Training
    * The goal is to create a joint embedding space for images and sentences such that closeness in this space can be interpreted as semantic similarity.
* Localization from embedding
    * Localization ability derives from the activation maps of the last convolutional layer.
>>![](https://github.com/TerenceCYJ/VP-SC-papers/raw/master/images/14.png)
