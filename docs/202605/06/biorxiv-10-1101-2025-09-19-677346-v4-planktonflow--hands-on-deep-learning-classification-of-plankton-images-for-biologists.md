---
title: "PlanktonFlow : hands-on deep-learning classification of plankton images for biologists"
title_zh: PlanktonFlow：面向生物学家的浮游生物图像深度学习分类实战工具
authors: "Walter, H., Gorzerino, C., Collinet, M., Porcon, B., Martignac, F., Edeline, E."
date: 2026-04-29
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.19.677346v4.full.pdf"
tags: ["query:sod"]
score: 6.0
evidence: 针对浮游生物分类中稀有类别的自动图像增强
tldr: 本研究开发了名为PlanktonFlow的Python流水线，旨在解决生物学家在处理大规模浮游生物图像时面临的深度学习应用门槛。该工具集成了图像预处理、数据增强、多种高性能CNN模型（如ResNet、EfficientNet等）的训练与优化，以及自动化推理功能。通过对FlowCAM获取的淡水浮游生物图像进行测试，证明了该工具在分类性能上优于传统工具EcoTaxa，为生物多样性观测提供了易用的自动化分类方案。
source: biorxiv
selection_source: fresh_fetch
motivation: 尽管高通量成像设备普及，但复杂的深度学习模型对许多生物学家而言仍难以实施和应用。
method: 开发了一个集成了图像预处理、四种主流CNN架构训练、超参数优化及推理功能的开源Python流水线。
result: 实验表明EfficientNet-B5在分类性能上表现最优，且所有优化的CNN模型均优于基准工具EcoTaxa。
conclusion: PlanktonFlow为非专业用户提供了高效、模块化的浮游生物图像分类工具，具有良好的社区扩展和跨领域应用潜力。
---

## 摘要
高通量图像采集设备极大地增强了我们观察生物多样性的能力。然而，对于许多生物学家来说，从海量图像集中提取生物学意义所需的高性能深度学习模型仍然难以实现。为了填补生物学家工具箱中的这一空白，我们开发了 PlanktonFlow，这是一个简化浮游生物图像分类学鉴定自动化流程的 Python 流水线。PlanktonFlow 使缺乏经验的用户能够轻松运行一整套流程，包括：(i) 自动图像预处理和稀有类别的增强；(ii) 训练多达四种不同的高性能卷积神经网络（CNN：ResNet、DenseNet、EfficientNet 和 YOLO）；(iii) 计算模型分类性能指标以选择最佳模型；以及 (iv) 对新图像集进行推理。PlanktonFlow 还包含易于微调模型超参数并优化模型性能的例程。我们以教程的形式展示了使用 PlanktonFlow 分析由 FlowCAM 产生的淡水浮游生物图像的过程，并比较了四种优化后的 CNN 架构的相对分类性能。为了与浮游生物学家使用的参考工具进行基准对比，我们进一步评估了 EcoTaxa Web 服务在无人工验证的纯预测模式下的分类性能。与之前对基准浮游生物数据集的研究一致，我们发现 EfficientNet-B5 实现了最高的宏平均 F1 分数，优于其他 CNN 模型，且所有模型均超过了 EcoTaxa。超参数优化是提高模型性能的关键。为了便于社区采用和进一步开发，PlanktonFlow 是开源的，配有详细文档，并具有模块化结构。我们预见未来的工作可以集成新的深度学习架构（例如视觉 Transformer、半监督学习），并在其他设备产生或其他分类群的图像上测试该流水线。

## Abstract
High throughput image-acquisition devices tremendously increase our capacity to observe biodiversity. However, for many biologists, the high-performance deep learning models that are needed to make biological sense out of very-large image sets remain difficult to implement.

To fill this gap in biologists toolkit, we developed PlanktonFlow, a Python pipeline that streamlines the automation of plankton-image taxonomic assignment. PlanktonFlow makes it easy for inexperienced users to run a whole sequence of (i) automated image pre-processing and augmentation of rare classes, (ii) training up to four different high-performance convolution neural networks (CNNs: ResNet, DenseNet, EfficientNet, and YOLO), (iii) computing model classification-performance metrics so as to choose the best-performing model, and (iv) running inference on novel image sets. PlanktonFlow further includes routines to easily fine tune model hyper-parameters and optimize models performances.

Using a tutorial style, we demonstrate the usage of PlanktonFlow to analyse freshwater-plankton images produced with the FlowCAM, comparing the relative classification performances of the four optimized CNN architectures. For a baseline comparison with a reference tool used by plankton biologists, we further assessed the classification performances of the EcoTaxa web-service when used without any eye validation in a pure-prediction mode. In line with a previous study on a benchmark plankton dataset, we found that EfficientNet-B5 achieved the highest macro-averaged F1 Score, outperforming other CNN models, which all surpassed EcoTaxa. Hyper-parameter optimization was key to improving model performances.

To ease an appropriation and further developments by the community, PlanktonFlow is open source, comes with a detailed documentation, and has a modular structure. We foresee that future work could integrate new deep-learning architectures (e.g., vision transformers, semi-supervised learning), and test the pipeline on images produced by other devices or from other taxonomic groups.