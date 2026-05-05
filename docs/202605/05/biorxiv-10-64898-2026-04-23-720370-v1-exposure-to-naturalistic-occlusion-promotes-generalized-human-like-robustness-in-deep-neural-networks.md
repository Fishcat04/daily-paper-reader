---
title: "Exposure to naturalistic occlusion promotes generalized, human-like robustness in deep neural networks"
title_zh: 接触自然遮挡可提升深度神经网络中广义的、类人的鲁棒性
authors: "Coggan, D. D., Tong, F."
date: 2026-04-27
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.23.720370v1.full.pdf"
tags: ["query:sod"]
score: 6.5
evidence: 使用自然遮挡物训练以提高目标识别鲁棒性
tldr: 本研究探讨了视觉训练数据对深度神经网络（DNN）遮挡鲁棒性的影响。通过对比仅使用清晰图像、人工几何形状遮挡图像以及自然物体遮挡图像训练的CNN和Transformer模型，并与30名人类受试者进行对比，发现使用自然遮挡物训练的模型在应对真实遮挡时表现出更接近人类的鲁棒性。研究表明，人类的遮挡鲁棒性源于学习区分自然物体，而非简单的局部识别，这对提升AI系统的现实世界鲁棒性具有重要意义。
source: biorxiv
selection_source: fresh_fetch
motivation: 深度神经网络在面对物体遮挡时通常比人类更脆弱，研究者旨在探究模拟自然视觉环境的训练数据是否能提升DNN的鲁棒性。
method: 研究者分别使用清晰图像、人工几何形状遮挡图像和自然物体遮挡图像训练模型，并将其性能与人类参与者的表现进行对比评估。
result: 实验发现，使用自然遮挡物训练的模型比使用人工遮挡物的模型在应对真实遮挡时更具鲁棒性，且表现出更接近人类的性能特征。
conclusion: 人类对遮挡的鲁棒性源于学习如何将自然物体相互分离，而目前常用的简单人工遮挡增强方法不足以提升模型在现实世界中的鲁棒性。
---

## 摘要
人类物体识别在挑战性条件下具有鲁棒性，例如当物体的视野因前景物体的遮挡而变得支离破碎时。相比之下，深度神经网络（DNN）通常更容易受到遮挡的影响，这表明人类视觉依赖于不同的机制。在本研究中，我们通过探究在使用更好地反映自然视觉遮挡特性的图像数据集进行训练时，DNN 是否会出现类人鲁棒性，从而研究了视觉经验（visual diet）在这些机制产生中的作用。我们训练了卷积和 Transformer DNN，使其仅对清晰图像、使用人工遮挡物（即几何形状）增强的图像或自然遮挡物（从照片中分割出的物体）增强的图像进行分类。随后，我们评估了 DNN 的遮挡鲁棒性，并将其性能表现与 30 名人类参与者进行了比较。我们发现，使用人工遮挡物训练的 DNN 对自然遮挡仍然脆弱，且与使用自然遮挡训练的 DNN 相比，表现出的类人性能较低。我们的研究结果表明，人类对视觉遮挡的鲁棒性源于学习将自然物体彼此分离，而不仅仅是学习从部分视图中识别物体。研究还暗示，常用的人工遮挡形式不适用于评估或提升 DNN 对现实世界遮挡的鲁棒性。

## Abstract
Human object recognition is robust to challenging conditions, such as when ones view of an object is fragmented due to an occluding foreground object. In comparison, deep neural networks (DNNs) are typically more susceptible to occlusion, suggesting that human vision relies on distinct mechanisms. Here, we investigated the role of visual diet in the emergence of these mechanisms by asking whether human-like robustness might arise in DNNs when trained with image datasets that better reflect the properties of occlusion in natural vision. We trained convolutional and transformer DNNs to classify clear images only, images augmented with artificial occluders (i.e., geometric shapes) or natural occluders (objects segmented from photographs). We then evaluated DNN occlusion robustness and compared their performance profiles with 30 human participants. We found that DNNs trained with artificial occluders remained vulnerable to natural occlusion and exhibited less human-like performance than those trained with natural occlusion. Our findings suggest that human robustness to visual occlusion arises from learning to disentangle natural objects from each other rather than simply learning to recognize objects from partial views. They also imply that commonly used forms of artificial occlusion are unsuitable for the evaluation or promotion of robustness to real-world occlusion in DNNs.