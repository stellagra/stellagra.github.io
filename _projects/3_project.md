---
layout: page
title: Deep Generative Models for Faces and Expressions
description: PhD project of René and ongoing research.
img: assets/img/deep_face4.png
importance: 3
category: research
related_publications: false
---

This page shall showcase the remarkable work of René Haas before and during his PhD.

## Generative Adversarial Networks

While [my own PhD project](https://stellagrasshof.com/projects/1_project/) was strictly based on non-neural-network methods, René expanded on my work and successfully combined old and new machine learning concepts.
Specifically, a factorization approach was employed in the latent space of StyleGAN. 
It turned out that using this set-up the rotation and expression of faces can be changed, as illustrated in the findings published 2021:

{% include figure.liquid loading="eager" path="assets/img/gen_face/2021_tensorgan_expr_transfer.png" title="" class="img-fluid rounded z-depth-1" width="80%" %}

Based on this work published in 2021, some improvements were presented in the follow-up published in 2022. 
We show-case the change of facial expression in the following. 

{% include figure.liquid loading="eager" path="assets/img/gen_face/2022_tensorgan_cvpr_ws.png" title="" class="img-fluid rounded z-depth-1" width="80%" %}

Comparing the two images, the individual features are better preserved than in the previous work. Find more details on this [website](https://github.com/renhaa/tensorgan). 

Since 2022, much progress has been made in the field. Particularly, the community has moved from Generative Adversarial Networks (GANs) to Diffusion Models. 

## Diffusion Models

In our latest publication we describe how to perform supervised and unsupervised editing of face images using diffusion models.  
Check out the [project webpage](https://github.com/renhaa/semantic-diffusion) for more details and code.

{% include figure.liquid loading="eager" path="assets/img/gen_face/fg2024_crop.png" title="" class="img-fluid rounded z-depth-1" width="100%" %}



## References
<div class="publications">
  {% bibliography -f papers -q @*[key=haas_discovering_2024]* %}
  {% bibliography -f papers -q @*[key=haas_controllable_2023]* %}
  {% bibliography -f papers -q @*[key=haas_tensor-based_2022]* %}  
  {% bibliography -f papers -q @*[key=haas_tensor-based_2021]* %}    
</div>