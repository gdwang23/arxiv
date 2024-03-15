**OccupancyDETR**
---
<!-- TOC -->
- [Introduction](#introduction)
    - [创新点](#创新点)
    - [缺点](#缺点)
- [3D occupancy decoder](#3d-occupancy-decoder)
<!-- TOC -->

# Introduction
# 创新点
  - 引入类似DETR的物体检测模块，指导3D语义占用网格的预测；使用检测到物体框作为位置先验,大幅提高白名单对象的IoU指标；
  - 
# 缺点
  - 路面没有框的先验，检测精度较低。在SemanticKitti上，相比于occFormer, IoU从58.85掉到36.68(DETR-BEV), 26.80 (DETR-3D).

# 3D Occupancy Decoder