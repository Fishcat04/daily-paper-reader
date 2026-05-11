---
title: Uncertainty-aware localization microscopy by variational diffusion
title_zh: 基于变分扩散的不确定性感知定位显微成像
authors: "Seitz, C., Liu, J."
date: 2026-05-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.01.722206v1.full.pdf"
tags: ["query:sod"]
score: 6.0
evidence: 深度学习用于密集小尺度图像中的荧光分子定位
tldr: 本研究针对单分子定位显微镜（SMLM）中高密度图像定位这一具有多解性的逆问题，提出了一种基于条件变分扩散模型（CVDM）的生成式建模框架。该方法通过对高分辨率核密度估计的分布进行建模，不仅实现了高保真度的超分辨率成像，还首次为定位显微镜提供了不确定性量化能力，有效解决了现有深度学习模型无法表达预测置信度的问题，对生物成像和图像修复具有重要意义。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有的深度学习定位显微镜方法在处理高密度图像时面临多解性挑战，且缺乏对预测结果的不确定性评估。
method: 提出一种基于条件变分扩散模型（CVDM）的生成式框架，通过建模高分辨率核密度估计的概率分布来处理低分辨率测量数据。
result: 实验证明该模型能够实现高保真度的超分辨率重建，并能有效评估回归过程中的不确定性。
conclusion: 该研究为定位显微镜引入了不确定性感知能力，为提高超分辨率成像的可靠性和图像修复提供了新的解决方案。
---

## 摘要
利用深度神经网络从图像中快速提取物理相关信息，在荧光显微成像及其在生物系统研究中的应用方面取得了重大进展。例如，在单分子定位显微成像（SMLM）中应用深度网络进行核密度（KD）估计，加速了细胞内密集标记结构的超分辨率成像。然而，在密集图像中定位荧光分子是一个具有潜在多解的困难逆问题。为了对该问题的解的概率分布进行建模，我们提出了一种基于条件变分扩散模型（CVDM）的 SMLM 核密度估计生成式建模框架。在该框架中，通过对高分辨率核密度估计的分布进行建模，训练 CVDM 在低分辨率测量值上执行定位任务。这种方法使我们能够探测核密度估计的分布结构并表达不确定性，而现有的定位显微成像深度模型目前尚不具备这一功能。我们证明了该模型能够实现高保真超分辨率，支持回归核密度估计的不确定性评估，并对单分子和超分辨率显微成像中的图像修复具有重要意义。

## Abstract
Fast extraction of physically relevant information from images using deep neural networks has led to significant advances in fluorescence microscopy and its application to the study of biological systems. For example, the application of deep networks for kernel density (KD) estimation in single-molecule localization microscopy (SMLM) has accelerated super-resolution imaging of densely labeled structures in the cell. However, localization of fluorescent molecules in dense images is a difficult inverse problem with potentially multiple solutions. To model a probability distribution of solutions to this problem, we propose a generative modeling framework for KD estimation in SMLM based on a conditional variational diffusion model (CVDM). In this framework, CVDM is trained to perform localization tasks on low-resolution measurements by modeling a distribution of high-resolution KD estimates. This approach allows us to probe the structure of the distribution on KD estimates and express uncertainty, which is not currently offered by existing deep models for localization microscopy. We demonstrate that this model permits high-fidelity super-resolution, enables the uncertainty estimation of regressed KD estimates, and has important implications for image restoration in single-molecule and super resolution microscopy.