---
layout: post
title:  "Self-Monitoring Agent for Vision-and-Language Navigation"
date:   2018-09-27
desc: "Self-Monitoring Navigation Agent via Auxiliary Progress Estimation"
keywords: "vision-and-language navigation"
categories: [Project]
tags:
icon:
---

<img align="right" src="../../../../static/assets/img/blog/einstein-scroll.png" width="8%">
<img align="right" src="../../../../static/assets/img/blog/salesforce-research.jpg" width="15%">
<br>


## **Self-Monitoring Navigation Agent via Auxiliary Progress Estimation**
[Chih-Yao Ma](https://chihyaoma.github.io/), [Jiasen Lu](https://www.cc.gatech.edu/~jlu347/), [Zuxuan Wu](http://zxwu.azurewebsites.net/), [Ghassan AlRegib](https://ghassanalregib.com/), [Zsolt Kira](https://www.cc.gatech.edu/~zk15/), [Richard Socher](https://www.socher.org/), [Caiming Xiong](http://www.stat.ucla.edu/~caiming/)<br>
<!-- Under Review, 2019<br> -->
International Conference on Learning Representations (ICLR), 2019<br>
**(Top 5% of reviews)**<br>
[[arXiv]](https://arxiv.org/abs/1901.03035)
[[OpenReview]](https://openreview.net/forum?id=r1GAsjC5Fm)
[[GitHub]](https://github.com/chihyaoma/selfmonitoring-agent)

---
## Abstract
The Vision-and-Language Navigation (VLN) task entails an agent following navigational instruction in photo-realistic unknown environments. This challenging task demands that the agent be aware of which instruction was completed, which instruction is needed next, which way to go, and its navigation progress towards the goal. In this paper, we introduce a self-monitoring agent with two complementary components: (1) visual-textual co-grounding module to locate the instruction completed in the past, the instruction required for the next action, and the next moving direction from surrounding images and (2) progress monitor to ensure the grounded instruction correctly reflects the navigation progress. We test our self- monitoring agent on a standard benchmark and analyze our proposed approach through a series of ablation studies that elucidate the contributions of the primary components. Using our proposed method, we set the new state of the art by a significant margin (8% absolute increase in success rate on the unseen test set).

---
## Proposed Concept
<p align="center">
<img src="../../../../static/assets/img/teasers/selfmonitoring.png?raw=true" width="75%">
</p>

---
## Qualitative Results

We qualitatively show how the agent navigates through unseen environments by following instructions as shown in the figure below.
In each figure, the agent follows the grounded instruction (at the top of the figure) and decides to move towards a certain direction (green arrow).
For the full figures and more examples of successful and failed agents in both unseen and seen environments, please see the supplementary material in our paper.

<p align="center">
<img src="../../../../static/assets/img/blog/selfmonitoring-demo.png?raw=true" width="75%">
</p>

<!-- --- -->
<!-- ## Citation -->
<!-- ``` -->
<!-- @inproceedings{ma2019selfmonitoring,
  title={Self-Monitoring Navigation Agent via Auxiliary Progress Estimation},
  author={Ma, Chih-Yao and Lu, Jiasen and Xu, Zuxuan and AlRegib, Ghassan and Kira, Zsolt and Socher, Richard and Xiong, Caiming},
  booktitle={Proceedings of the International Conference on Learning Representations (ICLR)},
  year={2019}
} -->
<!-- ``` -->