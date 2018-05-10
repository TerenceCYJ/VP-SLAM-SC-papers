## Semantics-aware Visual Localization under Challenging Perceptual Conditions

Tayyab Naseer, Gabriel L. Oliveira, Thomas Brox, Wolfram Burgard, ICRA, 2017

### Summary
- 提出一个新的数据集，数据集内图片为在德国弗莱堡市车载拍摄，包含appearance and structural changes （季节和天气差异），时间跨度为3年。并将训练图像的潜在的不确定区域标记为non-discriminative，将图像场景中几何稳定的结构标注为discriminative区域。

- 训练了一个DCNN模型用于图像中 discriminant regions 的密集像素分割（Up-Convilutional网络，用于提供包括几何稳定结构区域的场景图） 。从分割和原始图像中提取深度特征（deep features),并它们聚合成robust scene descriptor。采用稀疏随机投影（Sparse Random Projection）将高维的特征映射为低维。使用余弦距离匹配特征向量与特征库。

- 实验：

	1.实验数据集：Cityscapes、Virtual KITTI 、自己提出的数据集，使用了数据增强（缩放，旋转，颜色失真和偏度）
  
  2.鲁棒描述子性能评估：F1=2*(precision*recall)/(precision+recall)

  3.计算时间比较
  
### Strengths / Novelties
提出了图像描述方法，有效应对季节和天气等变化造成的室外场景图像特征差异。
### Weaknesses / Notes
仅提出了图像描述的方法，并从描述子的性能与其他几种描述子做比较，未在定位精度层面给出评判。
