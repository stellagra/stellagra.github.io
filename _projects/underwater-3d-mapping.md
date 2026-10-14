---
layout: page
title: Underwater Computer Vision and 3D Mapping
description: Vision for underwater inspection, from image segmentation to 3D mapping with video and sonar.
img: assets/img/publication_preview/2024_marnet_oceans.jpg
importance: 3
category: research
related_publications: false
---

# Motivation

Computer Vision tasks above water provide challenges. 
Underwater, the challenges intensify. While cameras provide rich visual detail, they struggle in murky water, or in poor lighting.  
Sonar, on the other hand, works in these conditions, but provides far less visual detail. 
Additionally, labelled real-world underwater data is scarce and expensive to collect, which limits how well machine learning models can be trained for these tasks.

Our research addresses these challenges via image segmentation and visual odometry towards reliable 3D mapping of underwater scenes.


# 3D Mapping of Underwater Scenes using Video and Sonar (2027–2029)

New project! More details tba

In 2026, we received funding from the [Orient Fund](https://orientsfond.dk/) and the [Danish Maritime Fund](https://dendanskemaritimefond.dk/it-universitetet-3d-mapping-of-underwater-scenes-using-video-and-sonar/) for the project *3D Mapping of Underwater Scenes using Video and Sonar*.

We will investigate when and how combining cameras and 3D sonar improves underwater 3D mapping compared to either technology alone. 

The project will make its data, evaluation methods, and reference implementations publicly available. 
Potential applications include the inspection of ship hulls, offshore energy installations, harbours, bridges, and pipelines.

**Open position:** A research assistant position for this project will be announced.


## Preliminary Related Work

Ongoing work with Olaya Álvarez-Tuñón: 3D Gaussian Splatting for underwater scenes.
Code and evaluation scripts are [publicly available](https://github.com/olayasturias/uw3dgs).

In ongoing student projects, we explore underwater scene reconstruction, e.g. by evaluating 3D Gaussian Splatting for underwater 3D reconstruction in degraded visual conditions.



# Image Segmentation for Underwater Inspection

Together with [Andrzej Wąsowski](http://www.itu.dk/people/wasowski/) and [Yury Brodskiy](https://www.linkedin.com/in/yurybrodskiy/), I co-supervised [Luiza Ribeiro Marnet](https://en.itu.dk/Research/PhD-Programme/PhD-Defences/PhD-Defences-2025/March/Luiza-Ribeiro-Marnet), who defended her PhD thesis *Vision-based classification for underwater safety critical applications* in March 2025. 
Her work showed how active learning can drastically reduce the amount of labelled data needed for pipeline segmentation in underwater inspection, and how models trained on simulated images can be adapted to real underwater footage. 
As part of this work, the [MarinaPipe dataset](https://github.com/remaro-network/MarinaPipe-dataset) was published.



# References
<div class="publications">
  {% bibliography -f papers -q @*[key=alvarez-tunon_gaussian_2026]* %}
  {% bibliography -f papers -q @*[key=alvarez-tunon_building_2026]* %}
  {% bibliography -f papers -q @*[key=marnet_bridging_2024]* %}
  {% bibliography -f papers -q @*[key=marnet_uncertainty_2024]* %}
</div>
