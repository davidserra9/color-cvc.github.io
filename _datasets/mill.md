---
layout: page
title: MILL
description: Multi-Illumination Low-Light Dataset for Evaluating Low-Light Image Enhancement Across Multiple Intensity Levels
img: assets/img/mill/teaser.jpg
importance: 1
category: work
related_publications: true
date: 11-2025
---

Existing low-light image enhancement (LLIE) datasets present critical limitations: they either contain a single severely underexposed image per scene or simulate brightness variations via camera parameter adjustments. This constraint limits real-world applicability, where low-light conditions span a continuous range of intensities.

To address this limitation, we introduce the **Multi-Illumination Low-Light (MILL)** dataset featuring multiple brightness levels per scene with fixed camera parameters. MILL enables comprehensive evaluation of enhancement algorithms across variable lighting conditions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mill/teaser.jpg" title="MILL Dataset" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Visual overview of the MILL dataset for low-light image enhancement.
</div>

### Dataset Highlights

- **50 scenes** captured across **11 intensity levels** (Levels 1-10 plus ground truth)
- **1,100 images** total with 6 different backgrounds and 98 unique objects
- Captured with **Nikon D5200 DSLR** and **Samsung Galaxy S7** smartphone
- Fixed camera parameters with programmable lighting for precise brightness control
- Two versions: **MILL-s** (600×400px) and **MILL-f** (Full-HD resolution)

### Full Project Page

For more details, interactive examples, dataset download links, and citation information, please visit the **[full MILL project page](/mill/)**.

---

**Paper**: [arXiv:2511.15496](https://arxiv.org/abs/2511.15496)
