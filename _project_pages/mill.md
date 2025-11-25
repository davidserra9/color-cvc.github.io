---
layout: page
title: "Evaluating Low-Light Image Enhancement Across Multiple Intensity Levels"
permalink: /mill/
description: ArXiv'25
img: assets/img/projects/mill/teaser.jpg
paper: https://arxiv.org/abs/2511.15496
code:
date: 2025-11-25
---

<div class="project-page">

<!-- Title -->
<h1 class="project-title">{{ page.title }}</h1>

<!-- Authors and Institutions -->
<div class="authors">
  <div class="author-block">
    <strong>Author Name 1</strong><sup>1</sup>,
    <strong>Author Name 2</strong><sup>1</sup>,
    <strong>Author Name 3</strong><sup>2</sup>
  </div>
  <div class="affiliations">
    <sup>1</sup>Computer Vision Center, Universitat Autònoma de Barcelona<br>
    <sup>2</sup>Institution Name
  </div>
</div>

<!-- Buttons -->
<div class="links" style="text-align: center; margin: 2rem 0;">
  <a href="https://arxiv.org/abs/2511.15496" class="btn btn-sm z-depth-0" role="button" target="_blank">
    <i class="fa-solid fa-file-pdf"></i> Paper
  </a>
  <a href="#" class="btn btn-sm z-depth-0" role="button">
    <i class="fa-brands fa-github"></i> Code
  </a>
  <a href="#" class="btn btn-sm z-depth-0" role="button">
    <i class="fa-solid fa-database"></i> Dataset
  </a>
  <a href="#citation" class="btn btn-sm z-depth-0" role="button">
    <i class="fa-solid fa-quote-left"></i> Citation
  </a>
</div>

<!-- Teaser -->
<div class="teaser">
  <div class="row">
    <div class="col-sm mt-3 mt-md-0">
      {% comment %}
      Uncomment when teaser image is available:
      {% include figure.liquid loading="eager" path="assets/img/projects/mill/teaser.jpg" title="MILL Teaser" class="img-fluid rounded z-depth-1" %}
      {% endcomment %}
      <p style="text-align: center; color: #999; padding: 3rem; background: #f5f5f5; border-radius: 8px;">
        [Teaser image placeholder - Add your teaser image at assets/img/projects/mill/teaser.jpg]
      </p>
    </div>
  </div>
  <div class="caption" style="margin-top: 1rem;">
    Visual overview of the MILL approach for multi-illuminant learning.
  </div>
</div>

<!-- Abstract -->
<div class="abstract" style="margin-top: 3rem;">
  <h2>Abstract</h2>
  <p>
    [Add your paper abstract here from the arXiv paper]
  </p>
  <p>
    This paper addresses the challenge of [fill in key contribution]. We propose [fill in method name], which [describe approach]. Our experiments demonstrate [key results].
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
<code>@article{mill2025,
  title={Multi-Illuminant Learning for Lighting-Invariant Image Matching},
  author={[Author List]},
  journal={arXiv preprint arXiv:2511.15496},
  year={2025}
}</code></pre>
</div>

<!-- Acknowledgments (Optional) -->
<div class="acknowledgments" style="margin-top: 3rem;">
  <h2>Acknowledgments</h2>
  <p>
    [Optional: Add funding acknowledgments, collaborators, etc.]
  </p>
</div>

</div>

<style>
.project-page {
  max-width: 900px;
  margin: 0 auto;
}

.project-title {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 2rem;
  line-height: 1.3;
}

.authors {
  text-align: center;
  margin-bottom: 2rem;
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

.links a.btn {
  margin: 0.25rem;
}
</style>
