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

<!-- Dataset Overview -->
<div class="method" style="margin-top: 3rem;">
  <h2>MILL Dataset</h2>
  <p>
    Existing low-light image enhancement (LLIE) datasets have two critical limitations: they either contain a single severely underexposed image per scene or simulate brightness variations through camera parameter adjustments. This constraint limits real-world applicability, where low-light conditions span a continuous range of intensities. Our experiments show that models trained on fixed brightness levels fail to generalize across different intensities, producing artifacts like oversaturation when tested on intermediate brightness levels.
  </p>
  <p>
    To address this limitation, we introduce the <strong>Multi-Illumination Low-Light (MILL)</strong> dataset featuring multiple brightness levels per scene with fixed camera parameters. All images were captured in a controlled indoor environment with programmable lighting to precisely control brightness levels. We used a Nikon D5200 DSLR camera and a Samsung Galaxy S7 smartphone, enabling evaluation across different sensor characteristics.
  </p>
  <p>
    <strong>Dataset Composition:</strong> We captured 50 scenes across 11 intensity levels (Levels 1-10 plus ground truth), totaling 1,100 images. The dataset includes 6 different backgrounds and 98 unique objects, with no overlap between train/validation and test sets. The split comprises 30 training scenes, 12 validation scenes, and 8 test scenes.
  </p>
  <p>
    <strong>Available Versions:</strong>
  </p>
  <ul>
    <li><strong>MILL-s (small):</strong> All images resized to 600×400 pixels for methods with computational constraints</li>
    <li><strong>MILL-f (full):</strong> DSLR images divided into 9 non-overlapping 2012×1340 patches (Full-HD resolution), expanding to 5,500 images; smartphone images at original 1560×1040 resolution</li>
  </ul>
  <p>
    All images were captured in RAW format and processed using Camera RAW, ensuring high-quality, well-calibrated data for robust training and evaluation of LLIE methods across varying illumination conditions.
  </p>
</div>

<!-- Dataset Examples Carousel -->
<div class="dataset-examples" style="margin-top: 3rem;">
  <h2>Dataset Examples</h2>
  <p style="margin-bottom: 1.5rem;">
    Explore example scenes at different illumination levels. Use the slider to adjust the brightness level and navigate between scenes.
  </p>

  <div class="carousel-container">
    <!-- Image Display -->
    <div class="carousel-image-wrapper">
      <img id="carousel-image" src="" alt="MILL Dataset Example" class="img-fluid rounded" style="width: 100%; max-height: 350px; object-fit: contain;">
    </div>

    <!-- Combined Navigation and Level Control -->
    <div class="level-slider" style="margin: 1.5rem auto; max-width: 600px;">
      <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 0.75rem;">
        <button id="prev-scene" class="btn btn-sm z-depth-0">
          <i class="fas fa-chevron-left"></i> Previous Scene
        </button>
        <label for="level-slider" style="margin: 0; font-weight: 500;">
          Illumination Level: <span id="level-value">1</span>
        </label>
        <button id="next-scene" class="btn btn-sm z-depth-0">
          Next Scene <i class="fas fa-chevron-right"></i>
        </button>
      </div>
      <input type="range" id="level-slider" min="1" max="11" value="1"
             style="width: 100%; cursor: pointer;">
      <div style="display: flex; justify-content: space-between; font-size: 0.85rem; color: #999; margin-top: 0.5rem;">
        <span>Darkest (1)</span>
        <span>Ground Truth (11)</span>
      </div>
    </div>
  </div>
</div>

<script>
// Carousel configuration
const sceneNumbers = [1, 12, 3, 4]; // Add more scene numbers as needed
const totalLevels = 11; // Levels 1-11
let currentSceneIndex = 0;
let currentLevel = 1;

// Update image source
function updateImage() {
  const sceneNum = sceneNumbers[currentSceneIndex];
  const imagePath = `{{ site.baseurl }}/assets/img/mill/Scene${sceneNum}_${currentLevel}.png`;
  document.getElementById('carousel-image').src = imagePath;
  document.getElementById('level-value').textContent = currentLevel;
}

// Event listeners
document.getElementById('prev-scene').addEventListener('click', () => {
  currentSceneIndex = currentSceneIndex > 0 ? currentSceneIndex - 1 : sceneNumbers.length - 1;
  updateImage();
});

document.getElementById('next-scene').addEventListener('click', () => {
  currentSceneIndex = currentSceneIndex < sceneNumbers.length - 1 ? currentSceneIndex + 1 : 0;
  updateImage();
});

document.getElementById('level-slider').addEventListener('input', (e) => {
  currentLevel = parseInt(e.target.value);
  updateImage();
});

// Initialize
updateImage();
</script>

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

/* Override title styling */
.post-title, .page-heading, h1.post-title {
  font-family: 'Helvetica Neue', Arial, sans-serif !important;
  font-size: 1.5rem !important;
  font-weight: 500 !important;
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
