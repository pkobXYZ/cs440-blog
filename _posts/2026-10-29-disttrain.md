---
layout: post
title: "DistTrain: Addressing Model and Data Heterogeneity with Disaggregated Training for Multimodal Large Language Models"
date: 2026-10-29
paper_authors: "Z. Zhang et al."
paper_venue: "SIGCOMM 2025"
paper_url: "https://dl.acm.org/doi/10.1145/3718958.3750472"
week: 6
tags: [ai, training, distributed-systems]
---

## Key Idea

This paper introduced DistTrain, a system for more efficiently distributing
training of multi-modal large language models. It does this by splitting up
different components of the training process that are typically treated as
monolithic. Model orchestration and data preprocessing are disaggregated.
The results 

## Critique

The paper primarily evaluates against Megatron-LM, when there are many other
training frameworks, such as Microsoft's DeepSpeed. The paper could have covered
these as well. Furthermore, it only tests with image-text models and not audio/video.
These can be future extensions to the work done in this paper.

## Connections

Like in _Raha: A General Tool to Analyze WAN Degradation_, the paper is solving
an optimization problem. It has to convert to a convex problem, just like in
Raha with MetaOpt.

