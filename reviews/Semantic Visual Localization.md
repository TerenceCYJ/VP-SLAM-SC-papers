## Semantic Visual Localization

Johannes L. Schonberger, Marc Pollefeys, Andreas Geiger, Torsten Sattler, CVPR, 2018

### Summary
- 输入：Color Image + Depth image；<br>
  database：images + camera poses；预处理阶段生成：全局3D语义地图（Global 3D semantic map）；<br>
  Query: 计算局部3D语义地图（Local 3D semantic map），建立3D-3D匹配;<br>
  输出：输入图片的Poses。
- 使用Bag of Semantic Word表示3D场景，BoSW是由descriptors计算得到。
- 实验：使用KITTI和NCLT验证。
- 生成描述符学习（Generative Descriptor Learning）：需要在不同的角度、光照等情况下识别出相同的目标，所以需要场景的语义理解来学习这种Invariant function。
### Strengths / Novelties
- 实验验证了在不同Viewpoint和Appearance改变的情景，仍能提供可靠的闭环和定位结果；
- 结合了语义和几何信息。
