---
title: "zFISHer: Automated 3D Registration, Detection, and Colocalization with Interactive Curation for Sequential Multiplexed FISH"
title_zh: zFISHer：用于序列多重 FISH 的自动化 3D 配准、检测、共定位及交互式人工辅助工具
authors: "Staller, S. A., Valentine, V., Burden, S."
date: 2026-05-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.19.726314v1.full.pdf"
tags: ["query:sod"]
score: 7.0
evidence: 在未对齐的z轴堆栈上进行自动点状物检测
tldr: zFISHer是一个基于napari的开源工具，旨在解决序列多重荧光原位杂交（FISH）图像分析中3D点位共定位分析耗时耗力的问题。它实现了从核分割、自动点位检测、多轮图像配准到交互式人工校正的全流程自动化，并引入Fishing Hook射线投射算法优化3D质心定位，显著提升了高通量空间分子图谱分析的效率和准确性。
source: biorxiv
selection_source: fresh_fetch
motivation: 针对序列多重FISH技术中三维数据集的点位共定位分析存在的手工操作繁琐、效率低下的瓶颈问题。
method: 开发了集成核分割、RANSAC配准、Fishing Hook射线投射算法及交互式编辑功能的开源napari插件。
result: 实现了端到端的自动化分析流程，支持高通量批处理，并能通过交互工具精确校正和分析三维空间中的分子共定位。
conclusion: zFISHer为复杂FISH数据集提供了一个高效、精确且用户友好的分析平台，极大地简化了空间转录组学研究中的数据处理环节。
---

## 摘要
序列多重荧光原位杂交 (FISH) 能够实现细胞单层中的空间分辨率分子分析，但在三维 (3D) 数据集中分析信号点 (puncta) 的共定位仍然是一个劳动密集型的瓶颈。zFISHer 是一款基于 napari 查看器构建的开源应用程序，它提供了序列 FISH 图像处理的全自动化，并结合了交互式用户辅助工具。zFISHer 提供成对 FISH 数据集的端到端分析，包括细胞核分割、未对齐 z-stacks 上的自动信号点检测、通过平移约束 RANSAC（可选 B 样条可变形扭曲）进行的多轮图像配准、信号点坐标到对齐空间的精确转换、共识细胞核生成、具有实时碰撞检测的交互式编辑，以及成对和三通道共定位分析及统计。这包括一种 Fishing Hook 光线投射算法，该算法通过识别沿摄像机光线的强度最大值，使用户能够在真实的 3D 质心处定位信号点，从而消除了手动 z 轴切片导航，并辅以亚体素体积优化。内置的批处理模式可实现多个实验数据集的高通量无人值守分析。

## Abstract
Sequential multiplexed fluorescence in situ hybridization (FISH) enables spatially resolved molecular profiling in cell monolayers, but analyzing puncta colocalization across three-dimensional (3D) datasets remains a labor-intensive bottleneck. zFISHer is an open-source application built on the napari viewer that provides complete automation of sequential FISH image processing in conjunction with interactive user-curation tools. zFISHer provides end-to-end analysis of paired FISH datasets, encompassing nuclear segmentation, automated puncta detection on unaligned z-stacks, multi-round image registration via translation-constrained RANSAC with optional B-spline deformable warping, precise transformation of puncta coordinates into aligned space, consensus nuclei generation, interactive editing with real-time collision detection, and pairwise and tri-channel colocalization analysis with statistics. This includes a Fishing Hook raycasting algorithm that enables users to locate puncta at their true 3D centroids by identifying intensity maxima along the camera ray, eliminating manual z-slice navigation, complemented by a sub-voxel volume optimization. The included batch processing mode enables high-throughput unattended analysis of multiple experimental datasets.