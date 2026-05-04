---
title: A novel attention mechanism for noise-adaptive and robust segmentation of microtubules in microscopy images
title_zh: 一种用于显微图像中微管噪声自适应且鲁棒分割的新型注意力机制
authors: "Ait Laydi, A., Cueff, L., Crespo, M., El Mourabit, Y., Bouvrais, H."
date: 2026-04-22
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.23.684152v3.full.pdf"
tags: ["query:sod"]
score: 6.5
evidence: 针对细小、密集结构的注意力机制
tldr: 本研究针对显微镜图像中微管分割面临的噪声、低对比度及细长结构交织等挑战，提出了一种新型噪声自适应注意力机制。通过将该机制集成到带有残差编码器的U-Net中，构建了轻量化模型ASE_Res_UNet。此外，研究还开发了合成数据集生成策略以解决标注难题。实验证明，该模型在合成和真实数据集上均表现优异，且具有良好的跨领域迁移能力，为生物医学研究提供了高效工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 针对显微镜图像中微管结构细长交织、噪声干扰严重以及精确标注获取困难等挑战，旨在提升分割的鲁棒性。
method: 提出ASE_Res_UNet模型，结合了改进的噪声自适应挤压激励（ASE）模块、残差学习以及合成数据增强策略。
result: 该模型在合成与真实微管数据集上均优于现有方法，且参数量更少，并成功迁移至血管和神经等曲线结构分割任务。
conclusion: 本研究通过提供基准数据集和高效的噪声自适应架构，为生物医学图像中的细长曲线结构分割提供了强有力的工具。
---

## 摘要
背景：在显微图像中分割细胞骨架丝状体对于研究其在细胞分裂和细胞内运输等细胞过程中的作用至关重要。然而，由于这些结构具有精细、密集且交织的特性，该任务极具挑战性。成像限制（如噪声、低对比度和荧光不均匀）进一步增加了分析的复杂性。虽然深度学习在分割大型、定义明确的生物结构方面取得了进展，但在这些不利条件下其性能往往会下降。其他挑战还包括获取曲线结构的精确标注以及在训练过程中处理严重的类别不平衡。结果：我们提出了一种新型的噪声自适应注意力机制，该机制扩展了挤压-激励（Squeeze-and-Excitation, SE）模块，以动态调整以适应不同的噪声水平。将其集成到带有残差编码器块的 U-Net 解码器中，得到了 ASE_Res_UNet，这是一种轻量级且高性能的模型。为了解决标注挑战，我们开发了一种合成数据集生成策略，确保了噪声图像中精细丝状体的准确标注，并生成了具有两个难度级别的合成数据集用于分割基准测试。我们系统地评估了损失函数和指标以减轻类别不平衡，确保了鲁棒的性能评估。ASE_Res_UNet 在噪声合成图像中有效地分割了微管，优于其消融变体。与具有替代注意力机制或不同架构的模型相比，它也表现出更优越的分割性能，同时所需的参数更少，使其在资源受限的环境中非常高效。在最新整理的真实显微数据集和最近重新标注的数据集上的评估表明，ASE_Res_UNet 在合成图像之外的微管分割中也具有有效性。对于这些数据集，ASE_Res_UNet 与最近一种共享两个细胞骨架预训练模型的合成数据驱动方法相比具有竞争力。重要的是，ASE_Res_UNet 在不同成像条件下对其他曲线结构（血管和神经）表现出很强的迁移能力。结论：本研究通过三个关键贡献推进了微管分割：（1）提供了两个基准数据集（合成和真实），填补了该任务标准化评估资源的空白；（2）引入了 ASE_Res_UNet，这是一种结合了噪声自适应注意力和残差学习的轻量级且鲁棒的模型；（3）验证了在合成和真实显微数据中的竞争性能。此外，我们展示了所提架构在各种曲线分割任务中的鲁棒性和通用性，显示了其在生物研究和医学诊断中更广泛应用的潜力。

## Abstract
BackgroundSegmenting cytoskeletal filaments in microscopy images is essential for studying their roles in cellular processes such as cell division and intracellular transport. However, this task is highly challenging due to the fine, densely packed, and intertwined nature of these structures. Imaging limitations--noise, low contrast, and uneven fluorescence--further complicate analysis. While deep learning has advanced segmentation of large, well-defined biological structures, its performance often degrades under such adverse conditions. Additional challenges include obtaining precise annotations for curvilinear structures and managing severe class imbalance during training.

ResultsWe introduce a novel noise-adaptive attention mechanism that extends the Squeeze-and-Excitation (SE) module to dynamically adjust to varying noise levels. Integrated into a U-Net decoder with residual encoder blocks, this yields ASE_Res_UNet, a lightweight yet high-performance model. To address annotation challenges, we developed a synthetic dataset generation strategy that ensures accurate annotations of fine filaments in noisy images, producing a synthetic dataset with two difficulty levels for segmentation benchmarking. We systematically evaluated loss functions and metrics to mitigate class imbalance, ensuring robust performance assessment. ASE_Res_UNet effectively segmented microtubules in noisy synthetic images, outperforming its ablated variants. It also demonstrated superior segmentation compared to models with alternative attention mechanisms or distinct architectures, while requiring fewer parameters, making it efficient for resource-constrained environments. Evaluation on a newly curated real microscopy dataset and a recently reannotated dataset highlighted ASE_Res_UNets effectiveness in segmenting microtubules beyond synthetic images. For these datasets, ASE_Res_UNet was competitive with a recent synthetic data-driven approach that shares two cytoskeleton pretrained models. Importantly, ASE_Res_UNet showed strong transferability to other curvilinear structures (blood vessels and nerves) across diverse imaging conditions.

ConclusionsThis work advances microtubule segmentation through three key contributions: (1) Providing two benchmark datasets (synthetic and real), addressing a critical gap in standardised evaluation resources for this task; (2) Introducing ASE_Res_UNet, a lightweight yet robust model combining noise-adaptive attention with residual learning; (3) Validating competitive performance across synthetic and real microscopy data. Additionally, we demonstrated the robustness and versatility of the proposed architecture across diverse curvilinear segmentation tasks, showcasing potential for broader applications in biological research and medical diagnosis.