---
layout: page
title: Expressive Personalized 3D Face Models
description: Short description of my PhD project.
img: assets/img/phd/face_model_slider.png
importance: 1
category: research
related_publications: false
---

Note: this page is still work in progress, including the selection of nice images created during my Phd. 


In 2012 I started my PhD project on initially on Talking Heads. The idea was to generate a 3D facial animation of a person with speech given text. 
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
        {% include figure.liquid loading="eager" path="assets/img/phd/david_cropped.gif" title="david2.5" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/phd/Uexpression_with_faces_color_dense.png" title="Uexpression" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/phd/facemodel.gif" title="facemodel" class="img-fluid rounded z-depth-1" %}
    </div>
</div>



## References
<div class="publications">
  {% bibliography -f papers -q @*[key=grashof_expressive_2019]* %}
  {% bibliography -f papers -q @*[key=brandt_uncalibrated_2019]* %}
  {% bibliography -f papers -q @*[key=awiszus_unsupervised_2018]* %}
  {% bibliography -f papers -q @*[key=grashof_projective_2017]* %}
  {% bibliography -f papers -q @*[key=grashof_apathy_2017]* %}
  {% bibliography -f papers -q @*[key=grashof_estimation_2015]* %}
  {% bibliography -f papers -q @*[key=grashof_performance_2013]* %}
</div>