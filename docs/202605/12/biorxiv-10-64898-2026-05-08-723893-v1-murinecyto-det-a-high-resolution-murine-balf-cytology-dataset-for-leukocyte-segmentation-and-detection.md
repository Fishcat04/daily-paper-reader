---
title: "MurineCyto-Det: A High-Resolution Murine BALF Cytology Dataset for Leukocyte Segmentation and Detection"
title_zh: MurineCyto-Det：用于白细胞分割与检测的高分辨率小鼠 BALF 细胞学数据集
authors: "Le, T. X., Tran, L.-A. T., Farabi, D. A., Wang, S., Phan, A. T. Q., Cormier, S. A., Taada, A., McGrew, D., Du, Y., Vu, L. D."
date: 2026-05-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.08.723893v1.full.pdf"
tags: ["query:sod"]
score: 8.5
evidence: 用于细胞检测和基准测试的高分辨率细胞学数据集
tldr: "针对临床前呼吸系统研究中缺乏公开小鼠支气管肺泡灌洗液（BALF）细胞学数据集的问题，本文推出了MurineCyto-Det数据集。该数据集包含333张高分辨率图像，涵盖五类细胞共14,551个标注实例，提供像素级分割掩码和边界框。通过基准测试，该数据集为细胞分割和检测任务提供了标准化资源，助力自动化分析方法的发展。"
source: biorxiv
selection_source: fresh_fetch
motivation: 临床前呼吸研究急需自动化的BALF细胞学分析工具，但目前缺乏公开且标注完善的小鼠相关图像数据集。
method: "构建了一个包含14,551个标注实例的高分辨率数据集，并使用代表性的分割和检测模型建立了基准性能。"
result: 实验结果验证了数据集的实用性，并揭示了类别不平衡、小目标及复杂形态带来的算法挑战。
conclusion: MurineCyto-Det为小鼠BALF细胞学分析提供了标准化的开发与评估资源，推动了该领域的自动化进程。
---

## 摘要
小鼠支气管肺泡灌洗液（BALF）细胞学的自动分析对于临床前呼吸系统研究具有重要意义，但由于缺乏公开可用且标注良好的小鼠 BALF 图像数据集，该领域的研究进展受到了限制。我们提出了 MurineCyto-Det，这是一个高分辨率的小鼠 BALF 细胞学数据集，包含 333 张尺寸为 1024 x 1024 像素的图像块，涵盖五个细胞学类别，并提供了像素级分割掩码和一一对应的边界框标注。该数据集包含 14,551 个标注的细胞实例，支持两项互补的分析任务：面向形态学的细胞分割和目标级细胞检测。为了建立可重复的基准基线，我们评估了具有代表性的分割和检测模型。结果证明了 MurineCyto-Det 的实际应用价值，同时也揭示了由类别不平衡、小目标尺寸、不规则细胞形态以及模糊的碎片状结构带来的现实挑战。MurineCyto-Det 为开发、评估和比较小鼠 BALF 细胞学分析的自动化方法提供了一个标准化的资源。该数据集可在 https://doi.org/10.5281/zenodo.17608677 公开获取。

## Abstract
Automated analysis of murine bronchoalveolar lavage fluid (BALF) cytology is important for preclinical respiratory research, yet progress has been limited by the lack of publicly available, well-annotated mouse BALF image datasets. We present MurineCyto-Det, a high-resolution murine BALF cytology dataset comprising 333 image tiles of size 1024 x 1024 pixels, annotated across five cytological categories with both pixel-level segmentation masks and one-to-one matched bounding boxes. The dataset contains 14,551 annotated cell instances and supports two complementary analysis tasks: morphology-oriented cell segmentation and object-level cell detection. To establish reproducible benchmark baselines, we evaluated representative segmentation and detection models. The results demonstrate the practical utility of MurineCyto-Det while highlighting realistic challenges arising from class imbalance, small object size, irregular cell morphology, and ambiguous debris-like structures. MurineCyto-Det provides a standardized resource for developing, evaluating, and comparing automated methods for murine BALF cytology analysis. The dataset is publicly available at https://doi.org/10.5281/zenodo.17608677.

---

## 论文详细总结（自动生成）

这篇论文介绍了一个名为 **MurineCyto-Det** 的新数据集，旨在解决临床前呼吸系统研究中缺乏高质量、公开的小鼠支气管肺泡灌洗液（BALF）细胞学图像数据的问题。以下是对该论文的结构化总结：

### 1. 核心问题与整体含义（研究动机和背景）
*   **研究动机**：BALF 细胞学分析是评估肺部炎症、感染和损伤的关键手段。虽然 AI 在人类细胞学领域取得了显著进展，但针对小鼠模型（免疫学和毒理学研究的核心）的自动化工具严重匮乏。
*   **核心问题**：目前缺乏专门针对小鼠 BALF 的公开标注数据集，且人类模型无法直接迁移至小鼠样本（由于形态、染色和细胞密度差异）。
*   **整体含义**：本文通过发布首个具有像素级分割和目标检测双重标注的高分辨率小鼠 BALF 数据集，为该领域的自动化分析建立了标准化的基准平台。

### 2. 方法论：核心思想与技术细节
*   **核心思想**：构建一个包含多种实验条件（如 RSV、H1N1 病毒感染及对照组）的综合数据集，并提供专家验证的精细标注。
*   **数据获取与处理**：
    *   从 5-6 周龄的 BALB/c 小鼠中采集 BALF，进行 H&E 染色。
    *   使用数字切片扫描仪以 40× 倍率捕捉高分辨率图像，并裁剪为 1024×1024 像素的图像块。
*   **标注协议**：
    *   **五类标注**：巨噬细胞/单核细胞、中性粒细胞、嗜酸性粒细胞、淋巴细胞、未知细胞/碎片。
    *   **双重标注**：首先进行像素级栅格分割（Mask），然后通过脚本自动生成一一对应的边界框（Bounding Box）。
    *   **质量控制**：由三名标注员独立标注，并由细胞学专家进行最终裁定。

### 3. 实验设计
*   **数据集划分**：333 张图像按 70%（训练）、15%（验证）、15%（测试）比例划分。
*   **任务与模型对比**：
    *   **语义分割任务**：对比了经典的卷积网络 **U-Net** 和基于 Transformer 的 **SegFormer**。
    *   **目标检测任务**：对比了一阶段检测器 **YOLOv8** 和二阶段检测器 **Faster R-CNN**。
*   **评价指标**：
    *   分割：像素准确率 (PA)、mIoU、Dice 分数、广义 Dice 分数 (GDS)。
    *   检测：精确率 (Precision)、召回率 (Recall)、F1 分数、mAP@0.50、mAP@0.50:0.95。

### 4. 资源与算力
*   **硬件配置**：使用了一台配备 **NVIDIA Ada 4000 GPU (16 GB VRAM)**、Intel 13900HX CPU 和 128 GB RAM 的工作站。
*   **软件环境**：PyTorch 2.7.1, CUDA 12.9, Windows 操作系统。
*   **训练细节**：分割模型训练 100 轮（Adam 优化器，初始学习率 1e-4）；检测模型中 YOLOv8 训练 100 轮，Faster R-CNN 由于内存占用较大，Batch Size 设为 2。

### 5. 实验数量与充分性
*   **实验规模**：共包含 14,551 个标注实例。实验涵盖了分割和检测两大主流视觉任务，并对比了不同架构（CNN vs. Transformer）和不同检测范式。
*   **充分性与公平性**：实验采用了固定的数据集划分以防止数据泄露，并使用了标准化的增强手段（翻转、仿射变换等）。虽然图像总数（333张）不算巨大，但实例数量足以支撑初步的深度学习基准测试。实验设计客观，反映了真实场景中的类别不平衡问题。

### 6. 主要结论与发现
*   **模型表现**：
    *   **分割**：SegFormer 在处理复杂边界和碎片识别上优于 U-Net；两种模型对主要类别（巨噬细胞、中性粒细胞）表现良好，但对稀有类别（淋巴细胞）表现较差。
    *   **检测**：YOLOv8 在各项指标上显著优于 Faster R-CNN，尤其是在小目标定位和稀有类别检测方面。
*   **挑战识别**：实验揭示了小鼠 BALF 分析的四大挑战：**类别严重不平衡**（淋巴细胞仅占 0.35%）、**目标尺寸小**、**细胞形态不规则**以及**背景碎片干扰**。

### 7. 优点
*   **高质量标注**：提供了像素级的分割掩码，这在细胞学数据集中较为罕见且极具价值。
*   **填补空白**：专门针对临床前研究最常用的小鼠模型，具有很强的科研实用性。
*   **双任务支持**：一套数据同时支持分割和检测，方便研究者根据需求选择形态学分析或高效计数。

### 8. 不足与局限
*   **类别不平衡**：嗜酸性粒细胞和淋巴细胞的样本量极少，可能导致模型在这些关键诊断类别上产生偏见。
*   **数据多样性限制**：目前仅包含 H&E 染色，未涵盖其他常用染色法（如 Diff-Quik）；且图像来源于特定型号的扫描仪，可能存在域偏移风险。
*   **规模尚小**：333 张图像对于训练极其鲁棒的通用模型来说仍显不足，未来需进一步扩充。

（完）
