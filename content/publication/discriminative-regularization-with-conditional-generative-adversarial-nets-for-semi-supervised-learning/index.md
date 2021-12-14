---
title: Discriminative regularization with conditional generative adversarial
  nets for semi-supervised learning
publication_types:
  - "1"
authors:
  - Qianqian Xie
  - admin
  - Min Peng
  - Yihan Zhang
  - Kaifei Peng
  - Hua Wang
author_notes: []
doi: ""
publication: In *IJCNN*
publication_short: ""
abstract: Existing generative adversarial networks (GANs) with manifold
  regularization for semi-supervised learning (SSL) have shown promising
  performance in image generation and semi-supervised learning (SSL), which
  penalize the smoothness of classifier over data manifold based on the
  smoothness assumption. However, the smoothness assumption is valid for data
  points in high density region while not hold for data points in low density
  region, thus they tend to misclassify boundary instances in low density
  region. In this paper, we propose a novel discriminative regularization method
  for semi-supervised learning with conditional generative adversarial nets
  (CGANs). In our method, the discriminative information from class conditional
  data distribution captured by CGANs is utilized to improve the discrimination
  of classifier. Different from regular manifold regularization, the
  discriminative regularization encourages the classifier invariance to local
  perturbations on the sub-manifold of each cluster, and distinct classification
  outputs for data points in different clusters. Moreover, our method can be
  easily implemented via the stochastic approximation without constructing the
  Laplacian graph or computing the Jacobian of classifier explicitly.
  Experimental results on benchmark datasets show that our method can achieve
  competitive performance against previous advanced methods.
draft: false
featured: false
tags:
  - neural network
  - deep learning
  - topic model
  - neural topic model
  - sparse topic model
projects: []
image:
  filename: ""
  focal_point: Smart
  preview_only: false
summary: ""
date: 2019-07-14T06:49:52.462Z
---
