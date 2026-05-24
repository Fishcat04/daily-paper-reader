---
title: "CRADLE: A Clinically Robust, Anatomy-Aware Post-Processing Framework for Infant GMA Landmark Tracking in 2D Videos"
title_zh: CRADLE：一种用于2D视频中婴儿GMA关键点追踪的临床鲁棒、解剖感知的后处理框架
authors: "Kaur, M., Abbasi, H., McMorland, A. J."
date: 2026-05-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.16.725614v1.full.pdf"
tags: ["query:sod"]
score: 6.0
evidence: 使用深度学习追踪视觉模糊的小关节
tldr: 本研究针对婴儿全身运动评估（GMA）中手持视频导致的遮挡、快速运动及关节模糊等姿态估计难题，提出了CRADLE后处理框架。该框架通过整合肢体长度约束、速度异常检测、解剖约束插值和卡尔曼滤波，对DeepLabCut检测的24个解剖关键点进行修正。实验证明，CRADLE在保持轨迹准确性的同时，显著降低了定位误差，尤其在临床意义重大的远端关节上表现优异，为下游神经发育风险分析提供了更可靠的数据支持。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有婴儿全身运动评估在真实场景视频中面临遮挡、快速运动和关节视觉模糊导致的姿态估计不准确挑战。
method: 提出CRADLE后处理框架，利用肢体长度约束、速度异常检测、解剖约束插值和卡尔曼滤波来修正24个解剖关键点的轨迹。
result: 实验结果显示该方法显著降低了平均绝对误差，特别是在临床关键的远端关节上实现了高达5像素的精度提升。
conclusion: CRADLE通过显著提高姿态轨迹的质量和解剖准确性，增强了婴儿神经发育风险自动评估下游分析的可靠性。
---

## 摘要
在不安运动期（fidgety period），准确的姿态估计是婴儿全身运动评估（GMA）自动化的核心，因为肢体的细微运动（尤其是远端关节）能够提供神经发育风险的信息。在现实场景中，由于遮挡、快速运动以及视觉模糊的小关节经常损害解剖准确性，从手持视频中进行鲁棒的2D姿态追踪仍具挑战性。我们提出了CRADLE，这是一个临床驱动、解剖感知的后处理流水线，旨在优化由DeepLabCut训练模型检测到的24个解剖关键点的婴儿2D运动轨迹。CRADLE集成了肢体分段长度约束、基于速度的异常检测、解剖约束插值和卡尔曼滤波，以纠正大规模定位失败和细微的持续性关节错位，且不主要依赖于置信度分数。通过平均绝对误差（MAE）、ΔMAE、平均正确关键点百分比（PCK）和净关键点纠正率与传统置信度阈值法的对比评估显示，该方法在保持准确轨迹的同时，持续减少或维持了误差，且在临床重要的远端关节上取得了最显著的提升。对于某些较小的远端关键点，平均改进达到了5个像素，大范围纠正发生的频率高于置信度阈值法，而定位良好的关节基本不受影响。掌指关节和跖趾关节等远端关键点的正向净纠正率进一步证实了纠正与退化之间的良好平衡。通过提高姿态轨迹质量，CRADLE增强了下游运动分析的可靠性。

## Abstract
Accurate pose estimation is central to automated infant General Movements Assessment during the fidgety period, when subtle limb movements, particularly at distal joints inform neurodevelopmental risks. Robust 2D pose tracking from handheld videos remains challenging in real-world settings, where occlusion, rapid motions, and visually ambiguous smaller joints frequently compromise anatomical accuracy.

We present CRADLE, a clinically motivated, anatomy-aware post-processing pipeline designed to refine infant 2D movement trajectories across 24-anatomocal landmarks detected by our DeepLabCut-trained model. CRADLE integrates segment-length constraints, velocity-based anomaly detection, anatomically constrained interpolation, and Kalman filtering to correct both large localization failures and subtle persistent joint misplacements without relying primarily on confidence scores.

Evaluations against conventional Confidence-Thresholding using Mean Absolute Error (MAE), {Delta}MAE, average Percentage of Correct Keypoints, and net keypoint correction rate showed consistently reduced or preserved error while maintaining accurate trajectories, with the strongest gains achieved at clinically important distal joints. Mean improvements reached up to 5 pixels for some smaller distal landmarks, large-magnitude corrections occurred more often than with Confidence-Thresholding, and well-localised joints remained largely unaffected. Positive net correction rates across metacarpophalangeal and metatarsophalangeal distal-landmarks further confirmed a favourable correction-degradation balance.

By improving pose trajectory quality, CRADLE enhances the reliability of downstream movement analysis.