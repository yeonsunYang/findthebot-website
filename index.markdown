---
layout: default
---

<span class="sys-name">EvalLM</span> ⚗️ is an interactive system that aids prompt designers in iterating on **prompts** by evaluating and comparing generated outputs on user-defined **criteria**. With the aid of an **LLM-based evaluation assistant**, the user can iteratively evolve **criteria+prompts** to distinguish more specific qualities in outputs and then improve the quality of outputs on these aspects.

<br/>

{: .sys-img}
![Animation of the overall workflow of EvalLM where users sample inputs from a dataset, generate outputs from each input using two different prompts, and then comparatively evaluate these outputs on user-defined criteria.](/assets/img/animation.gif)

------

## Interface

The main screen of the interface consists of three panels.

{: .sys-img}
![Main screen of EvalLM shows three panels. The generation panel shows text boxes for the prompt and task instruction, and buttons for input sampling. The evaluation panel shows text boxes for the criteria, buttons for evaluating, and stacked bar charts for the evaluation results.](/assets/img/interface.png)

<b>Generation Panel</b>: To generate outputs, the user defines their overall **task instruction** (A), two **prompts** they want to compare (B), and then **samples inputs** from a dataset (C) which will be used to test the prompts.

**Evaluation Panel**: To evaluate outputs, the user defines a set of evaluation **<a href="#criteria" target="_self">criteria</a>** (D). Then, after evaluating, they can verify the overall *evaluation* performance of each prompt (E) or, if they created a validation set, *validate* how automatic evaluations align with ground-truth evaluations (F).

**Data Panel**: This panel shows **<a href="#datarow" target="_self">data rows</a>** containing inputs, outputs, and evaluation results. 

<br/>

### <span id="criteria">Criteria</span>

{: .text-left}
<span class="sys-name">EvalLM</span> allows users to evaluate outputs on their own criteria specific to their application and/or context. 
<br/><br/>
To define a criteria, the user simply provides the criteria with a **name** (A) and **description** (B) in natural language.
<br/><br/>
To assist users in creating more effective and helpful criteria, the system automatically **reviews** their criteria (C) and provides **suggestions** (D) on how the criteria can be *refined*, *merged* and *split*.

{: .img-right}
![Criteria are represented as a set of text boxes that contain the name and description of the criteria. Suggested revisions are shown below the criteria.](/assets/img/criteria.png)

<br/>

### <span id="datarow">Data Row</span>

{: .sys-img}
![Data Rows in the interface display inputs, output pairs, and evaluation results. Clicking on evaluation results opens a panel that shows the explanation for that evaluation underneath the row.](/assets/img/datarow.png)

For each sampled **input** (A), the interface presents the **outputs** generated from each prompt side-by-side (B) and the **evaluation results** for each criteria next to the outputs (C). For each criteria, the evaluation results show which prompt produced the output that better satisfied that criteria.

If the user wants to see more details, they can click on one of these evaluations to see the assistant's **explanation** (D). To help the user match the explanation and outputs, the system also **highlights** spans from the outputs that were considered to be important when evaluating the criteria (E).

If the user selected to evaluate outputs on multiple trials, they can see the evaluations for **other trials** through the carousel (F). 

------

## Video Demo

See <span class="sys-name">EvalLM</span> in action in this Video Demo.

{% if site.video %}
<div class="video-wrapper">
  <iframe src="{{site.video}}&color=white&rel=0&modestlogo=1" id="yt-video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
{% endif %}

------

## Bibtex
<pre>
@inproceedings{10.1145/3613904.3642216,
author = {Kim, Tae Soo and Lee, Yoonjoo and Shin, Jamin and Kim, Young-Ho and Kim, Juho},
title = {EvalLM: Interactive Evaluation of Large Language Model Prompts on User-Defined Criteria},
year = {2024},
isbn = {9798400703300},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3613904.3642216},
doi = {10.1145/3613904.3642216},
booktitle = {Proceedings of the CHI Conference on Human Factors in Computing Systems},
articleno = {306},
numpages = {21},
keywords = {Evaluation, Human-AI Interaction, Large Language Models, Natural Language Generation},
location = {<conf-loc>, <city>Honolulu</city>, <state>HI</state>, <country>USA</country>, </conf-loc>},
series = {CHI '24}
}
</pre>

------

{: .logos}
[![Logo of KIXLAB](/assets/img/kixlab_logo.png)](https://kixlab.org)
[![Logo of KAIST](/assets/img/kaist_logo.png)](https://kaist.ac.kr)
[![Logo of NAVER](/assets/img/naver_logo.png)](https://www.facebook.com/NAVERAILAB)

{: .center .acknowledgement}
This research was supported by the **KAIST-NAVER Hypercreative AI Center**.
