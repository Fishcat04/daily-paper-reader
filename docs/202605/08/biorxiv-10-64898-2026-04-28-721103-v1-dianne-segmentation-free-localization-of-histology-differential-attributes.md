---
title: "DIANNE: Segmentation-Free Localization of Histology Differential Attributes"
title_zh: DIANNE：组织学差异属性的免分割定位
authors: "Domanskyi, S., Rubinstein, J. C., Sheridan, T. B., Thiesen, A., Noorbakhsh, J., Alcoforado Diniz, J., Ramasamy, R., Baker, D. S., Sheldon, R., Wu, Q., Kuchel, G., Robson, P., Chuang, J. H."
date: 2026-05-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.28.721103v1.full.pdf"
tags: ["query:sod"]
score: 6.0
evidence: 用于定位的正类Mixup增强
tldr: "DIANNE是一个针对组织病理学和空间组学图像的快速训练与推理框架。针对传统AI模型依赖大量手动标注且难以应对新空间表型的痛点，DIANNE引入了正类混合增强技术和基于基础模型的无分割定位方法。它仅需少量标注即可在数秒内完成全切片图像的差异化分类与定位，支持H&E、IHC及空间转录组等多种模态，为探索复杂组织结构和新颖空间表型提供了高效的交互式工具。"
source: biorxiv
selection_source: fresh_fetch
motivation: 传统的数字病理AI模型依赖耗时的手动预标注，难以快速适应新颖的空间生物学特征研究。
method: 提出DIANNE框架，利用正类混合增强技术和基础模型特征，实现无需分割的快速交互式训练与差异化属性定位。
result: 该方法仅需数十个标注块即可在数秒内完成全切片图像推理，并成功应用于肿瘤检测、组织结构识别及多模态数据分析。
conclusion: DIANNE为定量理解已知和新颖的空间表型提供了一个实用且高效的系统，显著提升了数字病理研究的灵活性。
---

## 摘要
病理学家引导的组织学和空间组学图像区分提供了对健康和疾病的见解，而数字病理学正利用人工智能来自动化此类评估。为了训练计算模型，目前的数字病理学方法依赖于前置的人工标注，而这些标注的生成非常耗时。预标注并不适用于研究新型空间行为——这是由空间分析技术进步驱动的一项主要需求——因为其标注标准和数据需求具有不确定性。为了应对这些挑战，我们提出了 DIANNE，这是一种基于训练时正类 Mixup 增强（Positive Class Mixup Augmentation）的数字病理学方法，用于空间差异属性的快速训练和推理。DIANNE 可以在工作站上数秒内计算出基于基础模型的、跨全切片 H&E 图像的差异分类器免分割定位，从而实现对空间生态位（spatial niches）的交互式研究。预测模型可以根据图像块或区域标注的变化进行实时重新训练，仅需几十个标注的图像块即可阐明跨切片的决定性生物学属性。我们展示了 DIANNE 在肿瘤检测、伪影识别以及胰腺、胎膜和肾脏组织结构探索方面的有效性。DIANNE 还为免疫组化（IHC）、多重免疫荧光以及配准的空间转录组+H&E 图像提供了类似的功能。DIANNE 在 Jupyter 工具包中实现，能够通过弱监督训练快速开发高分辨率分类器。DIANNE 为定量理解已知和新型空间表型提供了一个实用的系统。

## Abstract
Pathologist-guided distinctions within histology and spatial omic images provide insights into health and disease, with digital pathology leveraging artificial intelligence to automate such assessments. To train computational models, current digital pathology methods rely on upfront manual annotations, which are time-consuming to generate. Pre-annotation is poorly suited to investigating novel spatial behaviors--a major need driven by advances in spatial profiling--for which annotation criteria and data needs will be uncertain. To address these challenges, we present DIANNE, a digital pathology approach for rapid training and inference of spatial differential attributes based on train-time Positive Class Mixup Augmentation. DIANNE can compute foundation model-derived segmentation-free localization of differential classifiers across whole slide H&E images within seconds on a workstation, enabling interactive investigation of spatial niches. Predictive models can be re-trained in real-time in response to patch or regional annotation changes, clarifying determinative biological attributes across slides from only a few dozen annotated patches. We demonstrate the effectiveness of DIANNE for tumor detection, artifact identification, and exploration of pancreatic, fetal membranes and kidney tissue structures. DIANNE also provides analogous capabilities for IHC, multiplex immunofluorescence, and registered spatial transcriptomic+H&E images. DIANNE is implemented in a Jupyter toolkit, enabling rapid development of high-resolution classifiers from weakly-supervised training. DIANNE provides a practical system to quantitatively understand known and novel spatial phenotypes.