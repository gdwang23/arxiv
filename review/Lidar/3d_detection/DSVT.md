**DSVT**
---
<!-- TOC -->
- [dynamic-sparse-window-attention](#dynamic-sparse-window-attention)
  - [动态集合划分](#动态集合划分)
  - [旋转集合（窗口内）](#旋转集合窗口内)
  - [混合窗口分区（窗口间）](#混合窗口分区窗口间)
- [attention 3D pooling](#attention-3d-pooling)
- [perception model](#perception-model)
<!-- TOC-->

## dynamic sparse window Attention
### 动态集合划分
- 每个窗口共$N$个体素，划分为$S$个集合，每个集合$\tau$个体素；
- 切片取出第$j$个集合的体素特征$\mathcal{F}_j\in\mathbb{R}^{\tau\times C}$, 和空间坐标$\mathcal{O}_j\in\mathbb{R}^{\tau\times 3}$;
- 每个子集合有相同的voxel数目，
- 划分集合可以按照x轴，y轴排序，得到不同的集合；

### 旋转集合（窗口内）
DSVT block
- x-axis集合排序，索引体素特征；
- MHSA，多头自注意力；
- y-axis集合排序，索引体素特征；
- MHSA，多头自注意力； 

体素特征维度，$\mathcal{F}\in\mathbb{R}^{S\times \tau\times C}$， 索引维度$\mathcal{O}\in\mathbb{R}^{S\times \tau\times 3}$
### 混合窗口分区（窗口间）

## attention 3D pooling
## perception model