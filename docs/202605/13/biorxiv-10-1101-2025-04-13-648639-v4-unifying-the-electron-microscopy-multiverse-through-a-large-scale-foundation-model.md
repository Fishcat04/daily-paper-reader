---
title: Unifying the Electron Microscopy Multiverse through a Large-scale Foundation Model
title_zh: 通过大规模基础模型统一电子显微镜多重宇宙
authors: "He, L., Shi, R., Wang, W., Fang, G., Cai, Y., Ma, L."
date: 2026-05-12
pdf: "https://www.biorxiv.org/content/10.1101/2025.04.13.648639v4.full.pdf"
tags: ["query:sod"]
score: 6.0
evidence: 用于纳米级生物结构的多尺度嵌入
tldr: 针对电子显微镜（EM）图像分析中数据异质性和工作流碎片化的问题，本文推出了首个大规模EM基础模型EM-DINO。该模型基于包含500万张图像的EM-5M数据集预训练，能够捕捉多尺度特征。在此基础上开发的OmniEM架构在图像修复和分割任务中表现卓越，超越了特定任务模型和扩散模型，并支持从低分辨率输入生成高分辨率分割，为亚细胞结构分析提供了标准化工具包。
source: biorxiv
selection_source: fresh_fetch
motivation: 电子显微镜图像存在高度异质性和工作流碎片化，阻碍了跨任务的可扩展分析。
method: 构建了包含500万张图像的EM-5M数据集，并开发了预训练基础模型EM-DINO及统一密集预测架构OmniEM。
result: OmniEM在图像修复和2D/3D线粒体及多类细胞器分割任务中均优于现有特定任务模型，且能有效减少伪影。
conclusion: 该研究通过整合数据集、基础模型和工具插件，为标准化电子显微镜分析提供了端到端解决方案，加速了生物发现。
---

## 摘要
电子显微镜（EM）图像的准确分析对于探索纳米级生物结构至关重要，但数据的异质性和碎片化的工作流程阻碍了可扩展的洞察。图像基础模型在大规模、多样化的数据集上进行预训练，为学习跨任务的可迁移表示提供了一个稳健的框架。在此，我们介绍了 EM-DINO，这是首个在 EM-5M 上预训练的 EM 图像基础模型。EM-5M 是一个经过策划和标准化的超大规模 EM 语料库（包含 500 万张图像），涵盖了多种物种、组织、实验方案和分辨率。EM-DINO 的多尺度嵌入捕获了丰富的图像特征，支持多种应用，包括特定器官的模式识别、图像去重和高质量图像修复。基于这些表示，我们开发了 OmniEM，这是一种用于统一密集预测的 U 型架构，在图像修复和分割方面均优于特定任务模型。在修复基准测试中，OmniEM 的性能与 EM 专用扩散模型相当，同时减少了可能误导解释的伪影。在 2D 和 3D 线粒体分割以及多类细胞器分割任务中，它也优于以往的方法。此外，我们展示了 OmniEM 生成高分辨率分割结果的综合能力，即使输入是低分辨率图像，这为在遗留和高通量 EM 数据集中进行精细亚细胞分析提供了潜力。EM-5M、EM-DINO、OmniEM 以及集成的 Napari 插件共同构成了一个用于标准化 EM 分析的全面端到端工具包，推进了对细胞和亚细胞的理解，并加速了新型细胞器形态和疾病相关变化的发现。

## Abstract
Accurate analysis of electron microscopy (EM) images is essential for exploring nanoscale biological structures, yet data heterogeneity and fragmented workflows hinder scalable insights. Pretrained on large, diverse datasets, image foundation models provide a robust framework for learning transferable representations across tasks. Here, we introduce EM-DINO, the first EM image foundational model pretrained on EM-5M, a large curated and standardized EM corpus (5 million images) encompassing multiple species, tissues, protocols, and resolutions. EM-DINOs multi-scale embeddings capture rich image features that support multiple applications, including organ-specific pattern recognition, image deduplication, and high quality image restoration. Building on these representations, we developed OmniEM, a U-shaped architecture for unified dense prediction that achieves superior performance compared with task-specific models in both image restoration and segmentation. In restoration benchmarks, OmniEM matches the performance of the EM-specific diffusion model while reducing spurious structural artifacts that could mislead interpretation. It also outperforms previous methods across 2D and 3D mitochondrial segmentation, as well as multi-class organelle segmentation tasks. Furthermore, we demonstrate OmniEMs integrated capability to generate high-resolution segmentations from low-resolution inputs, offering the potential to enable fine-scale subcellular analysis in legacy and high-throughput EM datasets. Together, EM-5M, EM-DINO, OmniEM, and an integrated Napari plugin comprise a comprehensive end-to-end toolkit for standardized EM analysis, advancing cellular and subcellular understanding and accelerating the discovery of novel organelle morphologies and disease-related alterations.