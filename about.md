---
layout: single
title: About
permalink: /
author_profile: true
classes: wide
---


Hi, I'm Thierry. I am a PhD student in a joint program at Université de Sherbrooke (Canada) and Institut National des Sciences Appliquées (INSA) de Lyon (France). I work in the Videos & Images Theory and Analytics Laboratory (VITAL) and Center for Research in Acquisition and Signal Processing for Health (CREATIS) labs. 

My current work focuses on deep learning applied to medical image analysis. My current project is about the estimation of the deformation of the heart in cardiac ultrasound. I have previously worked on segmentation with a focus on uncertainty estimation. 

<h2>Featured Work</h2>

<div class="featured-work">

<!-- ------------------ PAPER 1 --------------------  -->
<details class="fw-item">
  <summary>
    <span class="fw-title">Generation of realistic cardiac ultrasound sequences with ground truth motion and speckle decorrelation
    </span>
    <span class="fw-hint fw-more">More</span>
    <span class="fw-hint fw-less">Less</span>
  </summary>

  <div class="fw-content">
    <p class="fw-desc">
    We propose a new physics-based ultrasound simulation pipeline to generate realistic ultrasound videos with ground truth motion to train deep learning tracking algorithms. More to come!
    </p>

    <details class="fw-sub">
      <summary>Abstract</summary>
      <p class="fw-abstract">
        Simulated ultrasound image sequences are key for training and validating machine learning algorithms for left ventricular strain estimation. Several simulation pipelines have been proposed to generate sequences with corresponding ground truth motion, but they suffer from limited realism as they do not consider speckle decorrelation. In this work, we address this limitation by proposing an improved simulation framework that explicitly accounts for speckle decorrelation. Our method builds on an existing ultrasound simulation pipeline by incorporating a dynamic model of speckle variation. Starting from real ultrasound sequences and myocardial segmentations, we generate meshes that guide image formation. Instead of applying a fixed ratio of myocardial and background scatterers, we introduce a coherence map that adapts locally over time. This map is derived from correlation values measured directly from the real ultrasound data, ensuring that simulated sequences capture the characteristic temporal changes observed in practice. We evaluated the realism of our approach using ultrasound data from 98 patients in the CAMUS database. Performance was assessed by comparing correlation curves from real and simulated images. The proposed method achieved lower mean absolute error compared to the baseline pipeline, indicating that it more faithfully reproduces the decorrelation behavior seen in clinical data.
      </p>
    </details>

    <figure class="fw-figure">
      <img src="{{ '/assets/simulation.gif' | relative_url }}" alt="Method overview">
      <figcaption>Example of videos generated with a previous simulation pipeline (Evain et al., IEEE TMI 2022) and our proposed simulation pipeline. Notice the difference in speckle patterns and realistic motion.</figcaption>
    </figure>

    <p class="fw-links">
      <a class="btn btn--primary" href="https://arxiv.org/abs/2509.05261" target="_blank" rel="noopener">Paper</a>
      <!-- <a class="btn" href="https://..." target="_blank" rel="noopener">Code</a> -->
    </p>
  </div>
</details>


<!-- ------------------ PAPER 2 --------------------  -->

<details class="fw-item">
  <summary>
    <span class="fw-title">Uncertainty Propagation for Echocardiography Clinical Metric Estimation via  Contour Sampling
    </span>
    <span class="fw-hint fw-more">More</span>
    <span class="fw-hint fw-less">Less</span>
  </summary>

  <div class="fw-content">
    <p class="fw-desc">
    We propose a contour-based uncertainty estimation method for echocardiography that predicts uncertainty in heart boundary locations, samples possible contours from it, and propagates that uncertainty to clinical metrics like volume and ejection fraction.
    </p>

    <details class="fw-sub">
      <summary>Abstract</summary>
      <p class="fw-abstract">
        Echocardiography plays a fundamental role in the extraction of important clinical parameters (e.g. left ventricular volume and ejection fraction) required to determine the presence and severity of heart-related conditions. When deploying automated techniques for computing these parameters, uncertainty estimation is crucial for assessing their utility. Since clinical parameters are usually derived from segmentation maps, there is no clear path for converting pixel-wise uncertainty values into uncertainty estimates in the downstream clinical metric calculation. In this work, we propose a novel uncertainty estimation method based on contouring rather than segmentation. Our method explicitly predicts contour location uncertainty from which contour samples can be drawn. Finally, the sampled contours can be used to propagate uncertainty to clinical metrics. Our proposed method not only provides accurate uncertainty estimations for the task of contouring but also for the downstream clinical metrics on two cardiac ultrasound datasets.
      </p>
    </details>

    <figure class="fw-figure">
      <img src="{{ '/assets/uncertainty_propagation.png' | relative_url }}" alt="Method overview">
      <figcaption>Overview of the method including contour uncertainty, contour sampling and uncertainty propagation.</figcaption>
    </figure>

    <p class="fw-links">
      <a class="btn btn--primary" href="https://arxiv.org/abs/2502.12713" target="_blank" rel="noopener">Paper</a>
      <a class="btn" href="https://github.com/ThierryJudge/contouring-uncertainty" target="_blank" rel="noopener">Code</a>
    </p>
  </div>
</details>


<!-- ------------------ PAPER 3 --------------------  -->

<details class="fw-item">
  <summary>
    <span class="fw-title">CRISP - Reliable Uncertainty Estimation for Medical Image Segmentation
    </span>
    <span class="fw-hint fw-more">More</span>
    <span class="fw-hint fw-less">Less</span>
  </summary>

  <div class="fw-content">
    <p class="fw-desc">
    We propose CRISP, a CLIP-like contrastive image–segmentation representation that learns a joint latent space of images and valid segmentations, then uses similarity to many stored latent vectors to produce anatomically consistent uncertainty maps.
    </p>

    <details class="fw-sub">
      <summary>Abstract</summary>
      <p class="fw-abstract">
        Accurate uncertainty estimation is a critical need for the medical imaging community. A variety of methods have been proposed, all direct extensions of classification uncertainty estimations techniques. The independent pixel-wise uncertainty estimates, often based on the probabilistic interpretation of neural networks, do not take into account anatomical prior knowledge and consequently provide sub-optimal results to many segmentation tasks. For this reason, we propose CRISP a ContRastive Image Segmentation for uncertainty Prediction method. At its core, CRISP implements a contrastive method to learn a joint latent space which encodes a distribution of valid segmentations and their corresponding images. We use this joint latent space to compare predictions to thousands of latent vectors and provide anatomically consistent uncertainty maps. Comprehensive studies performed on four medical image databases involving different modalities and organs underlines the superiority of our method compared to state-of-the-art approaches. 
      </p>
    </details>

      <figure class="fw-figure">
        <img src="{{ '/assets/crisp.png' | relative_url }}" alt="Method overview">
        <figcaption>Overview of the method for training [top] and inference [bottom].</figcaption>
      </figure>

      <p class="fw-links">
        <a class="btn btn--primary" href="https://arxiv.org/abs/2206.07664" target="_blank" rel="noopener">Paper</a>
        <a class="btn" href="https://github.com/ThierryJudge/CRISP-uncertainty" target="_blank" rel="noopener">Code</a>
      </p>
  </div>
</details>



