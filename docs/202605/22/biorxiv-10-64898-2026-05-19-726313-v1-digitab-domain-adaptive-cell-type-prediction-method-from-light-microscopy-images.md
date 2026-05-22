---
title: "DigitAb: Domain-Adaptive Cell Type Prediction Method from Light Microscopy Images"
title_zh: DigitAb：基于光学显微镜图像的领域自适应细胞类型预测方法
authors: "Lucarelli, N., Winfree, S., Sabo, A., Barwinska, D., Ferkowicz, M., Bowen, W., Singh, A., Chen, K., Tatke, A., Jen, K.-Y., Eadon, M. T., El-Achkar, T. M., Jain, S., Sarder, P."
date: 2026-05-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.19.726313v1.full.pdf"
tags: ["query:sod"]
score: 7.5
evidence: 显微图像中细胞类型预测的深度学习框架
tldr: "本研究开发了DigitAb深度学习框架，旨在直接从常规H&E染色切片中预测细胞类型，无需昂贵的多重免疫染色技术。通过利用Phenocycler技术生成的350万个细胞的高分辨率标注，该模型实现了对10种细胞类型的精确分割。结合对抗性领域自适应模块，DigitAb在肾移植和糖尿病肾病样本中表现出与临床金标准高度一致的预测能力，为临床病理提供了可扩展且无标记的细胞分析工具。"
source: biorxiv
selection_source: fresh_fetch
motivation: "旨在解决多重成像技术成本高、操作复杂且在临床实验室中难以普及的问题，实现从常规H&E图像中直接获取细胞组成信息。"
method: 开发了集成对抗性领域自适应模块的深度学习语义分割框架，利用大规模多重成像数据作为金标准进行训练。
result: 模型在10种细胞类型上达到了0.78的平衡准确率，并在肾移植排斥反应和糖尿病肾病的临床验证中显示出与金标准的高度一致性。
conclusion: DigitAb提供了一种高效、低成本且无需标记的细胞分割方案，能够显著提升常规组织病理学在临床诊断和生物医学研究中的应用价值。
---

## 摘要
组织学染色的光学显微成像在疾病诊断和研究中处于核心地位。通过免疫染色增强，可以揭示与临床效用和生物学机制相关的细胞组成及复杂性。Phenocycler 等新兴的多重成像技术显著增加了捕获细胞多样性的覆盖范围，但其成本高昂、技术要求高，且大多数临床实验室无法使用。我们开发了 DigitAb，这是一个深度学习框架，可直接从苏木精-伊红（H&E）染色切片中对细胞类型进行分类，从而无需专门的检测。利用 Phenocycler 成像，我们从四个多机构数据集的 29 个肾脏样本中生成了约 350 万个细胞的高分辨率真值，用于训练 10 种细胞类型的语义分割模型，实现了 0.78 的平衡准确率。通过采用集成的对抗性领域自适应模块，我们在来自肾移植和糖尿病样本的未标记且未测试的活检样本上测试了 DigitAb。我们能够仅通过组织学图像预测多种细胞类型，而无需使用任何特殊技术或免疫染色，并证明其与肾移植排斥反应中的临床金标准 Banff 方案以及糖尿病肾病的临床特征具有高度一致性。我们的云端工具 DigitAb 为研究和临床病理学提供了可扩展、易获取且无标记的细胞分割。

## Abstract
Light microscopy imaging with histological stains is central to disease diagnosis and research. It is enhanced with immunostaining to reveal cellular composition and complexity linked to clinical utility and biological mechanisms. Emerging multiplex imaging technologies like Phenocycler markedly increase the coverage to capture the cellular diversity but are costly, technically demanding, and inaccessible to most clinical laboratories. We developed DigitAb, a deep learning framework that classifies cell types directly from hematoxylin and eosin (H&E) stained slides, eliminating the need for specialized assays. Using Phenocycler imaging, we generated high-resolution ground truths for ~3.5 million cells from 29 human kidney samples across four multi-institutional datasets to train a semantic segmentation model for 10 cell types, achieving a balanced accuracy of 0.78. By employing an integrated adversarial domain adaptation module, we tested DigitAb on unlabeled and untested biopsy samples from kidney transplant and diabetic samples. We were able to predict several cell types just from histology images, without using any special technology or immunostains, and demonstrate high concordance with clinical gold-standard Banff schema in kidney transplant rejection, and clinical characteristics of diabetic nephropathy. Our cloud-based tool, DigitAb, provides scalable, accessible, label-free cellular segmentation for research and clinical pathology