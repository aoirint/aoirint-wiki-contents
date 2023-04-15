---
title: LoRA
description: 
published: true
date: 2023-04-15T05:24:04.133Z
tags: 
editor: markdown
dateCreated: 2023-04-15T04:55:34.377Z
---

LoRA（Low-Rank Adaptation）は、2021年にEdward Huらが提案した、大規模言語モデルを効率的にFine tuningする手法。

- <https://github.com/microsoft/LoRA>
- <https://arxiv.org/abs/2106.09685>

> An important paradigm of natural language processing consists of large-scale pretraining on general domain data and adaptation to particular tasks or domains. As we pre-train larger models, full fine-tuning, which retrains all model parameters, becomes less feasible. Using GPT-3 175B as an example – deploying independent instances of fine-tuned models, each with 175B parameters, is prohibitively expensive. We propose Low-Rank Adaptation, or LoRA, which freezes the pretrained model weights and injects trainable rank decomposition matrices into each layer of the Transformer architecture, greatly reducing the number of trainable parameters for downstream tasks. Compared to GPT-3 175B fine-tuned with Adam, LoRA can reduce the number of trainable parameters by 10,000 times and the GPU memory requirement by 3 times. LoRA performs on-par or better than finetuning in model quality on RoBERTa, DeBERTa, GPT-2, and GPT-3, despite having fewer trainable parameters, a higher training throughput, and, unlike adapters, no additional inference latency. We also provide an empirical investigation into rank-deficiency in language model adaptation, which sheds light on the efficacy of LoRA. We release a package that facilitates the integration of LoRA with PyTorch models and provide our implementations and model checkpoints for RoBERTa, DeBERTa, and GPT-2 at https://github.com/microsoft/LoRA.

cloneofsimoによりText to Image Diffusion Modelに応用した実装が公開された。

- <https://github.com/cloneofsimo/lora>

## 関連項目

- [LoRA Easy Training Scripts](/lora_easy_training_scripts)
