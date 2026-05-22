---
layout: default
permalink: /challenge/
title: BRAVO Challenge
---

# BRAVO Challenge

In conjunction with the Workshop on Uncertainty Quantification for Computer Vision, we are organizing a challenge on the robustness of autonomous driving in the open world. 
The 2025 BRAVO Challenge aims at benchmarking segmentation models on urban scenes undergoing diverse forms of natural degradation and realistic-looking synthetic corruptions. 

🔥 <b>[New]</b> In the 2025 edition, we extend the challenge with a new track on synthetic-domain training, while continuing the two real-domain training tracks from the BRAVO Challenge 2024.

<b>Top teams will be invited to present their solutions in a dedicated session at the UNCV workshop</b>

<b>For more information, please check the [BRAVO Challenge Repository](https://github.com/valeoai/bravo_challenge) and the [Challenge Task Website at ELSA](https://benchmarks.elsa-ai.eu/?ch=1&com=introduction).</b>



## Important Dates

All times are 23:59 CEST.

<ul>

{% for item in site.challengedl  %}

  <li>{{ item.item }}: <strong>{{ item.date }}</strong></li>

{% endfor %}

</ul>

## General rules

1. The task is semantic segmentation with pixel-wise evaluation performed on the 19 semantic classes of Cityscapes.
2. Models in each track must be trained using only the datasets allowed for that track.
3. Employing generative models for data augmentation is strictly forbidden.
4. All results must be reproducible. Participants must submit a white paper containing comprehensive technical details alongside their results. Participants must make models and inference code accessible.
5. Evaluation will consider the 19 classes of Cityscapes (see below).
6. Teams must register a single account for submitting to the evaluation server. An organization (e.g. a University) may have several teams with independent accounts only if the teams are not cooperating on the challenge.

## 2. The BRAVO Benchmark Dataset

We created the benchmark dataset with real, captured images and realistic-looking synthetic augmentations, repurposing existing datasets and combining them with newly generated data. The benchmark dataset comprises images from [ACDC](https://acdc.vision.ee.ethz.ch/), [SegmentMeIfYouCan](https://segmentmeifyoucan.com/), [Out-of-context Cityscapes](https://arxiv.org/abs/2108.00968), and new synthetic data.

Get the full benchmark dataset at the following link: [full BRAVO Dataset download link](https://drive.google.com/drive/u/4/folders/11-dnlbMjm8O_ynq1REuDYKOmHLqEhGYP).

The dataset includes the following subsets (with individual download links):

**bravo-ACDC:** real scenes captured in adverse weather conditions, i.e., fog, night, rain, and snow. ([download link](https://drive.google.com/drive/u/4/folders/1IW6-Tdfk2At6CrIIrA-QJF6CEcHgqqha) or directly from [ACDC website](https://acdc.vision.ee.ethz.ch/download))

  <div>
      <img src="{{ site.baseurl }}/assets/bravobenchmark/acdc/acdc1.png"   style="width: 19%; height: auto;"> 
      <img src="{{ site.baseurl }}/assets/bravobenchmark/acdc/acdc2.png" style="width: 19%; height: auto;"> 
      <img src="{{ site.baseurl }}/assets/bravobenchmark/acdc/acdc3.png" style="width: 19%; height: auto;"> 
      <img src="{{ site.baseurl }}/assets/bravobenchmark/acdc/acdc4.png" style="width: 19%; height: auto;"> 
      <img src="{{ site.baseurl }}/assets/bravobenchmark/acdc/acdc5.png" style="width: 19%; height: auto;">
  </div>

**bravo-SMIYC:** real scenes featuring out-of-distribution (OOD) objects rarely encountered on the road. ([download link](https://drive.google.com/drive/u/4/folders/1XnC9_7RzwZCWaDpP3iETbGt7Yvmg0MOg) or directly from [SMIYC website](https://segmentmeifyoucan.com/))

  <div>
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synrain/rain1.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/smiyc/smiyc2.jpg" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/smiyc/smiyc3.jpg" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/smiyc/smiyc4.jpg" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/smiyc/smiyc5.jpg" style="width: 19%; height: auto;">
  </div>

**bravo-synrain:** augmented scenes with synthesized raindrops on the camera lens. We augmented the validation images of Cityscapes and generated 500 images with raindrops. ([download link](https://drive.google.com/drive/u/4/folders/1onP6tUVSjV-qKWWLm6wiOZCB9U14_gQ6))

  <div>
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synrain/rain1.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synrain/rain2.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synrain/rain3.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synrain/rain4.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synrain/rain5.png" style="width: 19%; height: auto;">
  </div>

**bravo-synobjs:** augmented scenes with inpainted synthetic OOD objects. We augmented the validation images of Cityscapes and generated 656 images with 26 OOD objects. ([download link](https://drive.google.com/drive/u/4/folders/1KKt_25S69DBf8ZTxhOhELpLgS2gyyGnf))

  <div>
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synobjs/cheetah.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synobjs/chimpanzee.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synobjs/lion.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synobjs/panda.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synobjs/penguine.png" style="width: 19%; height: auto;"> 
  </div>

**bravo-synflare:** augmented scenes with synthesized light flares. We augmented the validation images of Cityscapes and generated 308 images with random light flares. ([download link](https://drive.google.com/drive/u/4/folders/13EpBXUY8BChoqfMxR5JhiyhqrzqLAO2y))

  <div>
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synflare/flare1.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synflare/flare2.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synflare/flare3.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synflare/flare4.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synflare/flare5.png" style="width: 19%; height: auto;">
  </div>

**bravo-outofcontext:** augmented scenes with random backgrounds. We augmented the validation images of Cityscapes and generated 329 images with random random backgrounds. ([download link](https://drive.google.com/drive/u/4/folders/1NoXqTQWxrj_yKMNRKLOd1rnn2TjqIaU5))

  <div>
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synooc/ooc1.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synooc/ooc2.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synooc/ooc3.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synooc/ooc4.png" style="width: 19%; height: auto;"> 
    <img src="{{ site.baseurl }}/assets/bravobenchmark/synooc/ooc5.png" style="width: 19%; height: auto;">
  </div>



## Challenge Tracks

We propose two tracks:

#### Track 1 – Single-domain training

In this track, you must train your models exclusively on the [Cityscapes dataset](https://www.cityscapes-dataset.com/). This track evaluates the robustness of models trained with limited supervision and geographical diversity when facing unexpected corruptions observed in real-world scenarios.

#### Track 2 – Multi-domain training

In this track, you must train your models over a mix of datasets, whose choice is strictly limited to the list provided below, comprising both natural and synthetic domains. This track assesses the impact of fewer constraints on the training data on robustness.

Allowed training datasets for Track 2:
- [Cityscapes](https://www.cityscapes-dataset.com/)
- [BDD100k](https://bdd-data.berkeley.edu/)
- [Mapillary Vistas](https://www.mapillary.com/datasets)
- [India Driving Dataset](https://idd.insaan.iiit.ac.in/)
- [WildDash 2](https://www.wilddash.cc/)
- [GTA5 Dataset](https://download.visinf.tu-darmstadt.de/data/from_games/) (synthetic)
- [SHIFT Dataset](https://www.vis.xyz/shift/) (synthetic)


#### 🔥 [New] Track 3 – Synthetic-domain training

In this track, you must train your models exclusively on the synthetic datasets. This track evaluates the robustness of models trained solely on synthetic data when facing corruptions observed in real-world scenarios.

Allowed training datasets for this track:
- [GTA5 Dataset](https://download.visinf.tu-darmstadt.de/data/from_games/) (synthetic)
- [SYNTHIA Dataset](https://synthia-dataset.net/) (synthetic)
- [UrbanSyn Dataset](https://www.urbansyn.org/) (synthetic)
- [SHIFT Dataset](https://www.vis.xyz/shift/) (synthetic)

<br>

<p>Supported by:</p>

<a href="https://elsa-ai.eu/">
<img src="{{ site.baseurl }}/assets/elsa-logo.png" class="img-responsive" style="width: 15%; height: auto;" alt="">
</a>
