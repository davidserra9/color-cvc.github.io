---
layout: page
title: "Evaluating Low-Light Image Enhancement Across Multiple Intensity Levels"
permalink: /mill/
img: assets/img/mill/teaser.jpg
paper: https://arxiv.org/abs/2511.15496
code:
date: 2025-11-25
---

<div class="project-page">

<!-- Authors and Institutions -->
<div class="authors">
  <div class="author-block">
    <strong>Maria Pilligua</strong><sup>1,2</sup>,
    <strong>David Serrano-Lozano</strong><sup>1,2</sup>,
    <strong>Pai Peng</strong><sup>3</sup>,<br>
    <strong>Ramon Baldrich</strong><sup>1,2</sup>,
    <strong>Michael S. Brown</strong><sup>4</sup>, and
    <strong>Javier Vazquez-Corral</strong><sup>1,2</sup>

  </div>
  <div class="affiliations">
    <sup>1</sup>Computer Vision Center, 
    <sup>2</sup>Universitat Autònoma de Barcelona, 
    <sup>3</sup>University of Wisconsin-Madison, 
    <sup>4</sup>York University
  </div>
</div>

<!-- Buttons -->
<div class="links" style="text-align: center; margin: 2rem 0;">
  <a href="https://arxiv.org/abs/2511.15496" class="btn z-depth-0" role="button" target="_blank">
    <i class="fa-solid fa-file-pdf"></i> Paper
  </a>
  <a href="#" class="btn z-depth-0" role="button">
    <i class="fa-brands fa-github"></i> Code
  </a>
  <a href="#" class="btn z-depth-0" role="button">
    <i class="fa-solid fa-database"></i> Dataset
  </a>
  <a href="#citation" class="btn z-depth-0" role="button">
    <i class="fa-solid fa-quote-left"></i> Citation
  </a>
</div>

<!-- Teaser -->
<div class="teaser">
  <div class="row">
    <div class="col-sm mt-3 mt-md-0">
      {% include figure.liquid loading="eager" path="assets/img/mill/teaser.jpg" title="MILL Teaser" class="img-fluid rounded z-depth-1" %}
    </div>
  </div>
  <div class="caption" style="margin-top: 1rem;">
    Visual overview of the MILL dataset for low-light image enhancement.
  </div>
</div>

<!-- Dataset Overview (Optional) -->
<div class="method" style="margin-top: 3rem;">
  <h2>MILL Dataset</h2>
  <p>
    
  </p>
</div>

<!-- Abstract -->
<div class="abstract" style="margin-top: 3rem;">
  <h2>Abstract</h2>
  <p>
    [Add your paper abstract here from the arXiv paper]
  </p>
  <p>
    Imaging in low-light environments is challenging due to reduced scene radiance, which leads to elevated sensor noise and reduced color saturation. Most learning-based low-light enhancement methods rely on paired training data captured under a single low-light condition and a well-lit reference. The lack of radiance diversity limits our understanding of how enhancement techniques perform across varying illumination intensities. We introduce the Multi-Illumination Low-Light (MILL) dataset, containing images captured at diverse light intensities under controlled conditions with fixed camera settings and precise illuminance measurements. MILL enables comprehensive evaluation of enhancement algorithms across variable lighting conditions. We benchmark several state-of-the-art methods and reveal significant performance variations across intensity levels. Leveraging the unique multi-illumination structure of our dataset, we propose improvements that enhance robustness across diverse illumination scenarios. Our modifications achieve up to 10 dB PSNR improvement for DSLR and 2 dB for the smartphone on Full HD images.
  </p>
</div>

<!-- Method Overview (Optional) -->
<div class="method" style="margin-top: 3rem;">
  <h2>Method Overview</h2>
  <p>
    [Optional: Add description of your method, additional figures, etc.]
  </p>
</div>

<!-- Results (Optional) -->
<div class="results" style="margin-top: 3rem;">
  <h2>Results</h2>
  <p>
    [Optional: Add key results, comparison tables, qualitative results, etc.]
  </p>
</div>

<!-- Citation -->
<div class="citation" id="citation" style="margin-top: 3rem;">
  <h2>Citation</h2>
  <p>If you find this work useful for your research, please cite:</p>
  <pre style="background-color: #f5f5f5; padding: 1rem; border-radius: 5px; overflow-x: auto;">
<code>@article{pilligua2025evaluating,
  title={Evaluating Low-Light Image Enhancement Across Multiple Intensity Levels},
  author={Pilligua, Maria and Serrano-Lozano, David and Peng, Pai and Baldrich, Ramon and Brown, Michael S and Vazquez-Corral, Javier},
  journal={arXiv preprint arXiv:2511.15496},
  year={2025}
}</code></pre>
</div>

<!-- Acknowledgments (Optional) -->
<div class="acknowledgments" style="margin-top: 3rem;">
  <h2>Acknowledgments</h2>
  <p>
    This work was supported by Grants PID2021-128178OB-I00 and PID2024-162555OB-I00 funded by MCIN/AEI/10.13039/ 501100011033 and by ERDF "A way of making Europe", and by the Generalitat de Catalunya CERCA Program. DSL also acknowledges the FPI grant from Spanish Ministry of Science and Innovation (PRE2022-101525). JVC also acknowledges the 2025 Leonardo Grant for Scientific Research and Cultural Creation from the BBVA Foundation. The BBVA Foundation accepts no responsibility for the opinions, statements and contents included in the project and/or the results thereof, which are entirely the responsibility of the authors. This research was also supported by the Natural Sciences and Engineering Research Council of Canada (NSERC) and the Canada Research Chairs (CRC) program.
  </p>
</div>

</div>

<style>
.project-page {
  max-width: 900px;
  margin: 0 auto;
}

.authors {
  text-align: center;
  margin-bottom: 2rem;
  margin-top: 2rem;
}

.author-block {
  font-size: 1.1rem;
  margin-bottom: 0.5rem;
}

.affiliations {
  font-size: 0.95rem;
  color: #666;
  line-height: 1.6;
}

.project-page .links a.btn {
  margin: 0.5rem;
  padding: 0.6rem 1.5rem;
  font-size: 1rem;
}
</style>
