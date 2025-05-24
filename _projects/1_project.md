---
layout: page
title: Expressive Personalized 3D Face Models from 3D Face Scans
description: PhD project of Stella and ongoing research.
img: assets/img/phd/face_model_slider.png
importance: 2
category: research
related_publications: false
---


In 2012 I started my PhD project initially on Talking Heads. The idea was to generate a 3D facial animation of a person with accompanying speech given text. 
Eventually, I reached an intermediate step with a textured coarse 3D model, as seen below on the left. 

The core of my final PhD project was a Higher-Order Singular Value Decomposition (HO-SVD) of a data tensor holding 3D face point clouds. Those were a result of 3D point correspondence estimation. For some databases a temporal alignment was necessary. 
This process unveiled an underlying expression subspace shown in the middle below. 
Using the decomposition and carefully designed constraints, we were able to make meaningful edits to the 3D face shapes as shown on the bottom right animation. 

<!-- 
![David](/assets/img/phd/david_cropped.gif)
![facemodel](/assets/img/phd/facemodel.gif)
![Uexpression](/assets/img/phd/Uexpression_with_faces_color_dense.png)
-->

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/phd/david_cropped.gif" title="david2.5" class="img-fluid rounded z-depth-1" width="120%" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/phd/Uexpression_with_faces_color_dense.png" title="Uexpression" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/phd/facemodel.gif" title="facemodel" class="img-fluid rounded z-depth-1" width="80%" %}
    </div>
</div>


# From Data to Aligned Data for Facial Models

Please find an overview of the whole process from 3D face scans to the 3D aligned faces in the following illustration:

{% include figure.liquid loading="eager" path="assets/img/phd/align_and_preprocess2.png" title="" class="img-fluid rounded z-depth-1" width="50%" %}

## Spatial Alignment

Multiple 3D face scans commonly differ in the number of points, and therefore need a general rigid alignment, followed by a registration and correspondence estimation procedure. 
In this domain prior knowledge in terms of facial landmarks is employed to improve the results. 

{% include figure.liquid loading="eager" path="assets/img/phd/face_correspondence.png" title="point correspondence" class="img-fluid rounded z-depth-1" width="50%" %}


## Temporal Alignment

When recording facial motion in 3D, the resulting 3D face scans might differ in their sequence length, hence requiring a *temporal alignment*. 
To achieve this in this project prior knowledge can be employed which is that the facial motion in the recorded sequences follows a common patter, which consists of an increase followed by an decrease of a depicted facial expression forming an emotion. 
Hence, an approach was formulated to estimate the expression intensity for each frame. In the following the resulting 1D signals encoding the intensity of facial expression per frame are used to compute an alignment of the 3D face scans, as illustrated.

{% include figure.liquid loading="eager" path="assets/img/phd/2018_awiszus_cvpr.png" title="temporal alignment" class="img-fluid rounded z-depth-1" width="50%" %}


# The 3D Face Model
After all the preprocessing and alignment, a balanced dataset with the same number of 3D points and number of frames has been obtained. This data can now be sorted into a matrix or data tensor and a factorisation method can be employed. 
In this work, the Higher-Order Singular Value Decomposition (HO-SVD) was employed to factorize the data tensor into different subspaces. Depending on the chosen order and dimension of the data tensor, new insights were gained. 
One of the main contributions was what we referred to as the *expression subspace*, which revealed a structure in a lower dimensional space. 




# References
<div class="publications">
  {% bibliography -f papers -q @*[key=grashof_multilinear_2021]* %}
  {% bibliography -f papers -q @*[key=grashof_expressive_2019]* %}
  {% bibliography -f papers -q @*[key=brandt_uncalibrated_2019]* %}
  {% bibliography -f papers -q @*[key=awiszus_unsupervised_2018]* %}
  {% bibliography -f papers -q @*[key=grashof_projective_2017]* %}
  {% bibliography -f papers -q @*[key=grashof_apathy_2017]* %}
  {% bibliography -f papers -q @*[key=grashof_estimation_2015]* %}
  {% bibliography -f papers -q @*[key=grashof_performance_2013]* %}
</div>