---
title: "Deep-Pose-Tracker: a unified model for behavioural analysis of Caenorhabditis elegans"
title_zh: Deep-Pose-Tracker：一种用于秀丽隐杆线虫行为分析的统一模型
authors: "Saha, D., Chaudhary, S., Vyas, D., Ghosh-Roy, A., Sharma, R."
date: 2026-05-24
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.23.689997v2.full.pdf"
tags: ["query:sod"]
score: 7.0
evidence: 用于小型生物自动检测与分析的深度学习模型
tldr: 本研究开发了Deep-Pose-Tracker (DPT)，这是一个基于YOLO的端到端深度学习模型，旨在自动化分析秀丽隐杆线虫的姿态动力学和运动行为。针对手动分析费时费力的问题，DPT实现了对线虫的自动检测与追踪，能够测量运动速度、方向及复杂的身体弯曲，并利用特征线虫分解进行低维姿态表示。该模型在保证高推理速度的同时表现出可靠的性能，为研究环境刺激下的生物行为提供了高效工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统的手动追踪和分析秀丽隐杆线虫行为的方法费时费力，亟需自动化工具来提高检测的准确性与效率。
method: 开发了基于YOLO的端到端深度学习模型Deep-Pose-Tracker，结合特征线虫分解技术实现对线虫姿态和运动的自动化分析。
result: 该模型在测试集上表现出可靠的性能和极高的推理速度，能够精准识别运动速度、方向及复杂的身体转弯。
conclusion: Deep-Pose-Tracker为研究人员提供了一个用户友好且高效的工具包，有助于深入探索不同环境刺激下的生物行为机制。
---

## 摘要
追踪和分析动物行为是神经科学和发育生物学等领域的关键步骤。例如，对秀丽隐杆线虫（C. elegans）的行为研究有助于理解生物体如何响应外部线索，以及特定的生理反应如何与瞬时或学习行为相关联。尽管通过运动模式和姿态动力学追踪行为已成为常规，但手动执行这些任务既费力又耗时。因此，这一过程的自动化对于准确、快速的检测和分析至关重要。为此，在本研究中，我们报告了 Deep-Pose-Tracker (DPT) 的开发，这是一种端到端深度学习模型，旨在自动分析秀丽隐杆线虫的姿态动力学和运动行为。该模型基于 YOLO (You Only Look Once)，能够自动检测和追踪线虫，同时测量关键的行为特征，如运动速度、方向、前进或后退运动以及复杂的身体弯曲（如 omega 转向）。此外，它还包含特征线虫（eigenworms）分解，以在低维空间中表示复杂的姿态动力学。该模型在评估和测试数据集上表现出可靠的性能，推理速度快且用户友好。因此，DPT 可以成为研究人员在不同环境刺激下研究行为的有价值工具包。

## Abstract
Tracking and analyzing animal behaviour is a crucial step in fields such as neuroscience and developmental biology. Behavioural studies in the nematode C. elegans, for example, help in understanding how organisms respond to external cues and how the specific physiological responses link to either instantaneous or learned behaviour. Although tracking behaviour through locomotion patterns and posture dynamics are routine, they become laborious and time-consuming tasks when performed manually. Automation of this process is therefore crucial for accurate and fast detection and analysis. To this end, in this work, we report the development of Deep-Pose-Tracker (DPT), an end-to-end deep learning model designed to automate the analysis of posture dynamics and locomotion behaviour of C. elegans. This YOLO (You Only Look Once)-based model enables automatic detection and tracking of worms while measuring essential behavioural features like motion speed, orientation, forward or reverse locomotion and complex body bends such as omega turns. In addition, it includes eigenworms decomposition to represent complex posture dynamics in a low-dimensional space. The model shows reliable performance on the evaluation and test dataset, with high inference speed, while being user-friendly. DPT, therefore, can be a valuable toolkit for researchers studying behaviours under different environmental stimuli.