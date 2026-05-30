---
title: A scutum-focused deep learning pipeline for species-level identification of Aedes aegypti and Aedes albopictus from citizen-science images
authors: "Kruthiventi, N., Hannum, A., Megahed, A., Chellappan, S., Carney, R., Kuusisto, F., Uelmen, J. A."
date: 2026-05-27
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.24.727056v1.full.pdf"
tags: ["query:sod"]
score: 6.0
evidence: 用于图像物种识别的深度学习流水线
tldr: 开发了一种鲁棒的深度学习流水线，用于从现实世界的公民科学图像中识别蚊子。
source: biorxiv
selection_source: fresh_fetch
motivation: 用于图像物种识别的深度学习流水线。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
BackgroundMosquito-borne diseases transmitted by Aedes aegypti and Aedes albopictus -- including dengue, Zika, chikungunya, and yellow fever -- depend critically on rapid and accurate vector identification. Although deep learning has achieved high accuracy on curated laboratory images, performance degrades substantially when applied to community-submitted photographs that vary widely in quality, framing, and background. We sought to develop a robust pipeline for distinguishing these two morphologically similar vectors from real-world citizen-science images.

MethodsWe compiled 2,112 mosquito images from the Global Mosquito Observation Database (GMOD) and assembled a multi-stage pipeline comprising: (i) a binary classifier to screen for mosquito presence; (ii) a YOLO-based object detector to localize specimens; (iii) an image-quality assessment module evaluating brightness, sharpness (Laplacian variance), contrast, and bounding-box ratio; (iv) Segment Anything Model (SAM) segmentation to isolate specimens from background clutter; and (v) a YOLO classifier trained on binary segmentation masks. To target the diagnostic characters used in conventional morphological taxonomy, we refined the pipeline to focus detection on the thoracic scutum -- the region bearing the lyre-shaped pale-scale pattern of Ae. aegypti and the median white stripe of Ae. albopictus.

ResultsBaseline YOLO classification on raw images achieved 30.95% accuracy for Ae. aegypti and 78.4% for Ae. albopictus, reflecting strong class imbalance and background noise. Augmentation alone provided only modest gains. The presence/absence classifier reached 90.52% accuracy, and the object detector localized mosquitoes with near-perfect precision. Whole-body SAM-mask classification improved overall accuracy to 68.21%. Refining the pipeline to scutum-focused classification yielded preliminary accuracies of 87.5% and 83.3% for Ae. albopictus and Ae. aegypti, respectively.

ConclusionsCommunity-sourced mosquito images, despite substantial noise and inconsistency, can support automated species-level vector surveillance when paired with a domain-informed, multi-stage deep-learning pipeline. Aligning machine attention with the morphological characters used by entomologists -- via scutum-focused detection -- delivers meaningful accuracy gains. This framework supports scalable citizen-science vector monitoring and lays the groundwork for integrating high-fidelity three-dimensional reference libraries to further strengthen real-world classifier performance.