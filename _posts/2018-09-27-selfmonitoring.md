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

<meta name="citation_title" content="Self-Monitoring Navigation Agent via Auxiliary Progress Estimation">
<meta name="citation_author" content="Ma, Chih-Yao">
<meta name="citation_author" content="Lu, Jiasen">
<meta name="citation_author" content="Wu, Zuxuan">
<meta name="citation_author" content="AlRegib, Ghassan">
<meta name="citation_author" content="Kira, Zsolt">
<meta name="citation_author" content="Socher, Richard">
<meta name="citation_author" content="Xiong, Caiming">
<meta name="citation_publication_date" content="2019/01/07">
<meta name="citation_conference_title" content="International Conference on Learning Representations (ICLR)">
<meta name="citation_pdf_url" content="https://arxiv.org/pdf/1901.03035.pdf">

<head>
<style>
.gunimage {
  display: inline-block;
  margin-left: auto;
  margin-right: auto;
  width: 15%;
}
.half {
  width:50%;
  float: left;
}
#images {
  text-align: center;
  width: 100%;
}
div.section_header {
  font-size: x-large;
  color: rgb(30,144,255);
}
</style>
</head>

<img align="right" src="../../../../static/assets/img/blog/einstein-scroll.png" width="8%">
<img align="right" src="../../../../static/assets/img/blog/salesforce-research.jpg" width="15%">
<br>


## **Self-Monitoring Navigation Agent via Auxiliary Progress Estimation**
[**Chih-Yao Ma**](https://chihyaoma.github.io/), [Jiasen Lu](https://www.cc.gatech.edu/~jlu347/), [Zuxuan Wu](http://zxwu.azurewebsites.net/), [Ghassan AlRegib](https://ghassanalregib.com/), [Zsolt Kira](https://www.cc.gatech.edu/~zk15/), [Richard Socher](https://www.socher.org/), [Caiming Xiong](http://www.stat.ucla.edu/~caiming/)<br>
<!-- Under Review, 2019<br> -->
International Conference on Learning Representations (ICLR), 2019<br>
**(Top 7% of reviews)**<br>
[[arXiv]](https://arxiv.org/abs/1901.03035)
[[OpenReview]](https://openreview.net/forum?id=r1GAsjC5Fm)
[[GitHub]](https://github.com/chihyaoma/selfmonitoring-agent)
[[Poster]](../../../../static/assets/pdf/iclr2019_poster_final-compressed.pdf)
<!-- <a href="static/assets/pdf/iclr2019_poster_final-compressed.pdf">[Poster]</a> / -->

---
<div class="section_header">Abstract</div>
The Vision-and-Language Navigation (VLN) task entails an agent following navigational instruction in photo-realistic unknown environments. This challenging task demands that the agent be aware of which instruction was completed, which instruction is needed next, which way to go, and its navigation progress towards the goal. In this paper, we introduce a self-monitoring agent with two complementary components: (1) visual-textual co-grounding module to locate the instruction completed in the past, the instruction required for the next action, and the next moving direction from surrounding images and (2) progress monitor to ensure the grounded instruction correctly reflects the navigation progress. We test our self- monitoring agent on a standard benchmark and analyze our proposed approach through a series of ablation studies that elucidate the contributions of the primary components. Using our proposed method, we set the new state of the art by a significant margin (8% absolute increase in success rate on the unseen test set).

---
<div class="section_header">Proposed Concept</div>

<p align="center">
<img src="../../../../static/assets/img/teasers/selfmonitoring.png?raw=true" width="75%">
</p>

---
<div class="section_header">Qualitative Results</div>

We qualitatively show how the agent navigates through unseen environments by following instructions as shown in the figure below.
In each figure, the agent follows the grounded instruction (at the top of the figure) and decides to move towards a certain direction (green arrow).
For the full figures and more examples of successful and failed agents in both unseen and seen environments, please see the supplementary material in our paper.

<p align="center">
<img src="../../../../static/assets/img/blog/selfmonitoring-demo.png?raw=true" width="75%">
</p>

---
<div class="section_header">Navigation Performance on Room-to-Room</div>


<span style="vertical-align:middle">
  <br>
  Our method achieves significant performance improvement compared to the state of the arts without data augmentation. We achieve 70% SR on the seen environment and 57% on the unseen environment while the existing best performing method achieved 63% and 50% SR respectively. When trained with synthetic data, our approach achieves slightly better performance on the seen environments and significantly better performance on both the validation unseen environments and the test unseen environments when submitted to the test server. We achieve 3% and 8% improvement on SR on both validation and test unseen environments. Both results with or without data augmentation indicate that our proposed approach is more generalizable to unseen environments.
</span>
<div>
<img style="display:block; margin-left: auto; margin-right: auto;" src="../../../../static/assets/img/blog/selfmonitoring-sota.png" width="75%">
</div>
<div style="clear: both;"></div>

---
<div class="section_header">Code and Paper</div>
<div id="images">
  <div class="half">
  <a href="https://github.com/chihyaoma/selfmonitoring-agent">
    <img class="gunimage" alt="idk" src="../../../../static/assets/img/blog/github-icon.png?raw=true">
    <p>GitHub</p>
  </a>
  </div>
  <div class="half">
    <a href="https://arxiv.org/abs/1901.03035">
    <img class="gunimage" alt="idk" src="../../../../static/assets/img/blog/paper-icon.png?raw=true">
    <p>arXiv</p>
    </a>
  </div>
</div>
<div style="clear: both;"></div>

---
<div class="section_header">Citation</div>
If you find this repository useful, please cite our paper:
<pre><code>
@inproceedings{ma2019selfmonitoring,
    title={Self-Monitoring Navigation Agent via Auxiliary Progress Estimation},
    author={Ma, Chih-Yao and Lu, Jiasen and Wu, Zuxuan and AlRegib, Ghassan and Kira, Zsolt and Socher, Richard and Xiong, Caiming},
    booktitle={Proceedings of the International Conference on Learning Representations (ICLR)},
    year={2019},
    url={https://arxiv.org/abs/1901.03035},
}
</code></pre>