---
title: Inductive Topic Variational Graph Auto-Encoder for Text Classification
publication_types:
  - "1"
authors:
  - Qianqian Xie
  - admin
  - Pan Du
  - Min Peng
  - Jian-Yun Nie
author_notes: []
doi: http://dx.doi.org/10.18653/v1/2021.naacl-main.333
publication: In *NAACL*
publication_short: ""
abstract: Graph convolutional networks (GCNs) have been applied recently to text
  classification and produced an excellent performance. However, existing
  GCN-based methods do not assume an explicit latent semantic structure of
  documents, making learned representations less effective and difficult to
  interpret. They are also transductive in nature, thus cannot handle
  out-of-graph documents. To address these issues, we propose a novel model
  named inductive Topic Variational Graph Auto-Encoder (T-VGAE), which
  incorporates a topic model into variational graph-auto-encoder (VGAE) to
  capture the hidden semantic information between documents and words. T-VGAE
  inherits the interpretability of the topic model and the efficient information
  propagation mechanism of VGAE. It learns probabilistic representations of
  words and documents by jointly encoding and reconstructing the global
  word-level graph and bipartite graphs of documents, where each document is
  considered individually and decoupled from the global correlation graph so as
  to enable inductive learning. Our experiments on several benchmark datasets
  show that our method outperforms the existing competitive models on supervised
  and semi-supervised text classification, as well as unsupervised text
  representation learning. In addition, it has higher interpretability and is
  able to deal with unseen documents.
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
date: 2021-06-01T06:44:38.764Z
---
