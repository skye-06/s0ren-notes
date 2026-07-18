---
title: Markdown 功能示例
description: 用于验证公式、表格、代码、图片和中文内部链接。
tags:
  - 示例
  - Markdown
---

# Markdown 功能示例

> 本页仅用于功能验证，请替换为真实学习笔记。

## 数学公式

伪距观测方程可写为：

$$
\rho_i = \lVert \mathbf{x} - \mathbf{s}_i \rVert
+ c(\delta t_r - \delta t_i) + I_i + T_i + \varepsilon_i
$$

其中 $\mathbf{x}$ 为接收机位置，$\mathbf{s}_i$ 为第 $i$ 颗卫星的位置。

## 表格

| 误差项 | 典型处理方式 | 备注 |
| --- | --- | --- |
| 卫星钟差 | 广播星历或精密钟差改正 | 与产品精度有关 |
| 电离层延迟 | 模型改正或双频组合 | 具有频率相关性 |
| 对流层延迟 | 经验模型与参数估计 | 与高度角有关 |

## 代码

```python
import numpy as np

satellite = np.array([15_600_000.0, 7_540_000.0, 20_140_000.0])
receiver = np.array([-2_300_000.0, 5_000_000.0, 3_200_000.0])
geometric_range = np.linalg.norm(satellite - receiver)

print(f"{geometric_range / 1_000:.3f} km")
```

## 本地图片

![GNSS 几何关系示意图](../assets/gnss-geometry.svg)

## 内部链接

- 前往 [[GNSS与卫星导航/index|GNSS 与卫星导航]]
- 前往 [[SLAM与融合定位/index|SLAM 与融合定位]]
- 返回 [[index|课程复习]]
