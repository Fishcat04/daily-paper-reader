---
title: Pushing the ceiling of species-level mapping in a hyperdiverse tropical forest with multi-temporal segmentation and airborne hyperspectral classification
title_zh: 利用多时相分割和机载高光谱分类提升高度多样化热带森林物种级制图的上限
authors: "Ball, J. G. C., Jaffer, S., Laybros, A., Prieur, C., Jackson, T. D., Madhavapeddy, A., Barbier, N., Vincent, G., Coomes, D."
date: 2026-05-05
pdf: "https://www.biorxiv.org/content/10.1101/2024.06.24.600405v4.full.pdf"
tags: ["query:sod"]
score: 6.0
evidence: 用于树冠检测的多时相分割与特征融合
tldr: "本研究针对高多样性热带雨林物种制图难题，提出了一种结合多时相无人机RGB影像分割与航空高光谱分类的两步法。在法属圭亚那的实验中，通过Mask R-CNN和共识融合技术提升了树冠分割精度，并利用LDA分类器实现了对169个树种的识别，最终成功制图了约70%的林冠区域，显著突破了以往研究在物种数量上的限制。"
source: biorxiv
selection_source: fresh_fetch
motivation: 热带雨林结构复杂且物种极度丰富，导致传统遥感技术难以实现大面积、高精度的物种级制图。
method: 采用Mask R-CNN结合多时相共识融合技术进行树冠分割，并利用航空高光谱数据配合线性判别分析进行多物种分类。
result: "树冠分割F1分数提升至0.78，物种分类加权F1达到0.75，成功覆盖了约70%的林冠面积并识别出169个物种。"
conclusion: 该方法大幅提升了热带雨林物种制图的物种覆盖广度，但分类精度仍受限于训练数据量及特定站点的光谱条件。
---

## 摘要
热带森林冠层的物种级地图对于生物多样性监测、保护规划和碳核算至关重要，但这些森林的结构复杂性和物种丰富度使得远程分类具有挑战性。本研究评估了在法属圭亚那 Paracou 野外站的高度多样化湿润森林中应用两步制图法的局限性与可能性。首先，我们利用卷积神经网络（Mask R-CNN）从 10 次重复的无人机（UAV）RGB 调查中描绘单株树冠，并通过时相共识融合方法结合不同日期的预测结果，将平均分割 F1 分数从 0.68（单日期）提高到 0.78（10 个日期），覆盖了约 86% 的冠层面积。其次，我们利用单次机载高光谱采集（416-2500 nm，1 米分辨率）数据，通过多种机器学习分类器对每个树冠进行物种分类，并在涵盖 169 个物种的 3,186 个经野外验证的树冠上进行了训练和测试（这些树冠选自包含 239 个物种、3,256 个树冠的有标签样本池；见第 2.6 节）。线性判别分析（LDA）达到了最高准确率（加权 F1 = 0.75），但表现并不均衡：重复交叉验证（20 x 5 折）显示，在任何给定的折数中，平均有 50 个物种（95% 置信区间：41-63）的 F1 >= 0.7，其中 38 个物种平均维持在这一水平，15 个物种表现可靠（>= 80% 的折数），而许多训练样本较少的稀有物种仍无法分类（宏平均 F1 = 0.48）。结合分割和分类，我们估计景观中约 70% 的冠层面积被正确映射到了物种。波段重要性和消融分析确定远红边（748-775 nm）是最具信息量的光谱区域，红光、绿光和短波红外（SWIR）也有次要贡献。虽然这些结果代表了相比以往仅限于 20 个以下物种的研究的重大进展，但我们提醒，准确性在很大程度上取决于训练数据的可用性、特定地点的光谱条件以及单次采集设计，且其对其他地点和传感器的泛化能力仍有待验证。

## Abstract
Species-level maps of tropical forest canopies are needed for biodiversity monitoring, conservation planning, and carbon accounting, yet the structural complexity and species richness of these forests make remote classification challenging. Here we evaluate the limits and possibilities of a two-step mapping approach applied to hyperdiverse moist forest at the Paracou Field Station, French Guiana. First, we delineate individual tree crowns from ten repeat UAV RGB surveys using a CNN (Mask R-CNN) and combine predictions across dates via a temporal consensus-fusion method, improving mean segmentation F1 from 0.68 (single date) to 0.78 (ten dates) and covering approximately 86% of canopy area. Second, we classify the species of each crown from a single airborne hyperspectral acquisition (416-2500 nm, 1 m resolution) using several machine learning classifiers trained and tested on 3,186 field-verified crowns spanning 169 species (drawn from a labelled pool of 3,256 crowns across 239 species; see Section 2.6). Linear Discriminant Analysis (LDA) achieved the highest accuracy (weighted F1 = 0.75), though performance was uneven: repeated cross-validation (20 x 5-fold) showed that on average 50 species (95% CI: 41-63) attained F1 >= 0.7 in any given fold, with 38 maintaining this level on average and 15 doing so reliably (>= 80% of folds), while many rare species with few training examples remained unclassifiable (macro-average F1 = 0.48). Combining segmentation and classification, we estimate that approximately 70% of the landscapes canopy area was correctly mapped to species. Band-importance and ablation analyses identified the far-red edge (748-775 nm) as the most informative spectral region, with secondary contributions from the red, green, and SWIR. While these results represent a substantial advance over previous studies limited to fewer than 20 species, we caution that accuracy is strongly conditioned by training data availability, site-specific spectral conditions, and the single-acquisition design, and that generalization to other sites and sensors remains to be demonstrated.