---
layout: base 
title: DNAttend
description: ML Frameowork for predicting patient non-attendance
permalink: DNAttend.html
---

# {{page.title}}

DNAttend trains two models independently; a baseline logistic regression model and a CatBoost model. The CatBoost model is trained via a cross-validated randomised hyper-parameter search with over-fit detection. In addition, over-fit detection is performed using a holdout validation set to determine the optimal boosting iterations. 

Output probability of both models are calibrated via cross-validation. 

Finally, decision thresholds are tuned, using the training dataset, to optimise either the ROC or F1 score.

You can find the [code here](https://github.com/nhsx/dna-risk-predict/tree/main)

RAP level: **Silver**

A view of the [Code documentation](https://nhsx.github.io/dna-risk-predict/) can be seen in the iframe below.

<iframe src="https://nhsx.github.io/dna-risk-predict/" width="100%" height="600" frameborder="0" scrolling="yes"></iframe>