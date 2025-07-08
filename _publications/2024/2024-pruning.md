---
title:          "Dynamic Vocabulary Pruning in Early-Exit LLMs"
date:           2024-12-1 00:01:00 +0800
selected:       false
pub:            "ENLSP Workshop, NeurIPS"
pub_date:       "2024"
abstract: >-
   Increasing the size of large language models (LLMs) has been shown to lead to better performance. However, this comes at the cost of slower and more expensive inference. To address this, we propose dynamically pruning the vocabulary at test time for each token. Specifically, the vocabulary is pruned at one of the initial layers, and the smaller vocabulary is then used throughout the rest of the forward pass. Our experiments demonstrate that such post-hoc dynamic vocabulary pruning improves the efficiency of confidence estimation in early-exit LLMs while maintaining competitive performance.


cover:          /assets/images/covers/early.png
authors:
  - Jort Vincenti*
  - Karim Abdel Sadek*
  - Joan Velja*
  - Matteo Nulli*
  - Metod Jazbec#
links:
  Paper: https://arxiv.org/abs/2410.18952
  Reviews: https://github.com/MatteoNulli/Vocabulary_pruning/tree/main
---
