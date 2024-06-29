---
layout: single
title:  "Data In Disguise: Getting More From Less with AI"
date: 2024-03-11
tags: "Data Augmentation Large Language Models Shapely Additive Explanation"
header:
    overlay_image: "assets/image/ML2-Augment.jpg"
---
Data Augmentation \| Large Language Models \| Shapely Additive Explanation


The study explores using LLMs like ChatGPT and Claude, along with the Shapley Additive Explanations (SHAP) algorithm, 
to create synthetic data for enhancing emotion detection models. A logistic regression model trained on a combination
of real and LLM-generated synthetic data achieved comparable accuracies up to 78.5% and 78.8% respectively, demonstrating
the viability of using LLMs to effectively mimic real data distributions. Key factors include providing LLMs with data exemplars
and using SHAP to identify emotion-associated keywords to guide the generation process. The study highlights the potential of LLMs
to overcome data constraints and unlock AI capabilities through informed prompt engineering and interpretability methods.

Snippet of what the data used in this study
<img src="{{ site.baseurl }}/assets/image/ml2-dataset.jpg" alt="Emotion">

**Results**

**Improvements in Model Accuracy with Addition of Supplementary Data**
<img src="{{ site.baseurl }}/assets/image/ml2-resutls.jpg" alt="Result">

**Progression of Accuracy as Real and LLM-Generated Data are Added**
<img src="{{ site.baseurl }}/assets/image/ml2-graph.jpg" alt="graph">

Overall, the results of this paper highlight the immense potential of leveraging large language models to
generate high-quality synthetic data, thereby helping organizations overcome data scarcity challenges and take advantage of the full capabilities
of state-of-the-art AI systems, particularly in the context of emotion detection or sentiment analysis tasks.
However, it is important to note that the key to unlocking this insight lies in the process of prompt engineering,
which involves carefully crafting the prompts given to LLMs. In this study, the prompt engineering process was informed by two crucial components:
1. Exemplars: A set of 40 real data samples were provided as exemplars to the
LLMs, allowing them to grasp the desired structure, tone, and style of the
target textual data.
2. SHAP-derived keywords: The Shapley Additive Explanations (SHAP) algorithm was employed to identify the most influential words that contribute
to the prediction of each emotion class (anger and joy). <br>

These SHAP-derived keywords were then incorporated into the prompts, guiding
the LLMs to generate synthetic data that accurately reflects the linguistic patterns
associated with each emotion. By combining these two components, the prompt engineering process ensured that the LLMs had access to both representative examples
and the most salient features of the real data

For a more detailed report you can access the paper and code [here](https://github.com/NRLTing-git/my-projects/tree/main/Data%20In%20Disguise%3A%20Getting%20More%20From%20Less%20with%20AI)
