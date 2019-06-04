---
layout: post
title:  "The Regretful Navigation Agent for Vision-and-Language Navigation"
date:   2019-02-25
desc: "The Regretful Agent: Heuristic-Aided Navigation through Progress Estimation"
keywords: "vision-and-language navigation"
categories: [Project]
tags:
icon:
---

<meta name="citation_title" content="The Regretful Agent: Heuristic-Aided Navigation through Progress Estimation">
<meta name="citation_author" content="Ma, Chih-Yao">
<meta name="citation_author" content="Wu, Zuxuan">
<meta name="citation_author" content="AlRegib, Ghassan">
<meta name="citation_author" content="Xiong, Caiming">
<meta name="citation_author" content="Kira, Zsolt">
<meta name="citation_publication_date" content="2019/03/05">
<meta name="citation_conference_title" content="Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)">
<meta name="citation_pdf_url" content="https://arxiv.org/pdf/1903.01602.pdf">

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


## **The Regretful Agent: Heuristic-Aided Navigation through Progress Estimation**
[**Chih-Yao Ma**](https://chihyaoma.github.io/), [Zuxuan Wu](http://zxwu.azurewebsites.net/), [Ghassan AlRegib](https://ghassanalregib.com/), [Caiming Xiong](http://www.stat.ucla.edu/~caiming/), [Zsolt Kira](https://www.cc.gatech.edu/~zk15/)<br>
IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2019 **(Oral)**<br>

[[arXiv]](https://arxiv.org/abs/1903.01602)
[[GitHub]](https://github.com/chihyaoma/regretful-agent)

---
<div class="section_header">Abstract</div>
As deep learning continues to make progress for challenging perception tasks, there is increased interest in combining vision, language, and decision-making. Specifically, the Vision and Language Navigation (VLN) task involves navigating to a goal purely from language instructions and visual information without explicit knowledge of the goal. Recent successful approaches have made in-roads in achieving good success rates for this task but rely on beam search, which thoroughly explores a large number of trajectories and is unrealistic for applications such as robotics. In this paper, inspired by the intuition of viewing the problem as search on a navigation graph, we propose to use a progress monitor developed in prior work as a learnable heuristic for search. We then propose two modules incorporated into an end-to-end architecture: 1) A learned mechanism to perform backtracking, which decides whether to continue moving forward or roll back to a previous state (Regret Module) and 2) A mechanism to help the agent decide which direction to go next by showing directions that are visited and their associated progress estimate (Progress Marker). Combined, the proposed approach significantly outperforms current state-of-the-art methods using greedy action selection, with 5% absolute improvement on the test server in success rates, and more importantly 8% on success rates normalized by the path length.

---
<div class="section_header">Proposed Concept</div>

<p align="center">
<img src="../../../../static/assets/img/teasers/regretful.png?raw=true" width="75%">
</p>

---
<div class="section_header">Qualitative Results</div>

The below figure shows the qualitative outputs of our model during successful navigation in unseen environments. 
In the example at the left side, the agent made a mistake at the first step, and the estimated progress at the second step slightly decreases.
The agent then decides to rollback, after which the progress monitor significantly increases. 
Finally, the agent stopped correctly as instructed. 
At the middle, we show an example where the agent correctly goes up the stairs but incorrectly does it again rather than turning and finding the TV as instructed. 
Note that the progress monitor increases but only by a small amount; this demonstrates the need for learned mechanisms that can reason about the textual and visual grounding and context, as well as the resulting level of change in progress. 
In this case the agent then correctly decides to rollback and successfully walked into the TV room. 
At the right side, the agent misses the stairs, resulting in a very small progress increase. 
The agent decides to rollback as a result. 
Upon reaching the goal, the agent's progress estimate is 99%.
Please refer to the Appendix for the full trajectories and unsuccessful examples.

<p align="center">
<img src="../../../../static/assets/img/blog/regretful-demo.png?raw=true" width="75%">
</p>

---
<div class="section_header">Navigation Performance on Room-to-Room</div>


<span style="vertical-align:middle">
  <br>
  We evaluate our proposed Regretful Agent on the Room-to-Room dataset for Vision-and-Language Navigation task.
  our method achieves significant performance improvement over the existing approaches.
  We achieved 37% SPL and 48% SR on the validation unseen set and outperformed all existing work.
  Our best performing model achieves 41% SPL and 50% SR on validation unseen set when trained with the synthetic data.
  We demonstrate absolute 8% SPL improvement and 5% SR improvement on the test server over the current state-of-the-art method.
</span>
<div>
<img style="display:block; margin-left: auto; margin-right: auto;" src="../../../../static/assets/img/blog/regretful-sota.png?raw=true" width="75%">
</div>
<div style="clear: both;"></div>

---
<div class="section_header">Code and Paper</div>
<div id="images">
  <div class="half">
  <a href="https://github.com/chihyaoma/regretful-agent">
    <img class="gunimage" alt="idk" src="../../../../static/assets/img/blog/github-icon.png?raw=true">
    <p>GitHub</p>
  </a>
  </div>
  <div class="half">
    <a href="https://arxiv.org/abs/1903.01602">
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
@inproceedings{ma2019theregretful,
    title={The Regretful Agent: Heuristic-Aided Navigation through Progress Estimation},
    author={Ma, Chih-Yao and Wu, Zuxuan and AlRegib, Ghassan and Xiong, Caiming and Kira, Zsolt},
    booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
    year={2019},
    url={https://arxiv.org/abs/1903.01602},
}
</code></pre>