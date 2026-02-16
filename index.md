---
layout: page
title: "GRAPE: Gaussian Rendering for Accelerated Pixel Enhancement"
description: "Fast & lightweight arbitrary-scale super-resolution with 2D Gaussian splatting"
---

# GRAPE: Gaussian Rendering for Accelerated Pixel Enhancement (Brings Fast and Lightweight Arbitrary Super-Resolution)

<div style="margin-top:8px; font-size: 1.05em;">
  <strong>Jung In Jang</strong><sup>1</sup> &nbsp; · &nbsp;
  <strong>Kyong Hwan Jin</strong><sup>1</sup>
</div>
<div style="margin-top:4px; color:#666;">
  <sup>1</sup>Korea University, Republic of Korea
</div>

<div style="margin-top:14px; display:flex; gap:10px; flex-wrap: wrap;">
  <a class="btn btn-primary" href="static/paper.pdf" target="_blank" rel="noopener">Paper (temp)</a>
  <a class="btn btn-outline-primary" href="https://github.com/mulkkog/GRAPE" target="_blank" rel="noopener">Code (GitHub)</a>
  <a class="btn btn-outline-primary" href="https://youtu.be/LwlF6hZ54ng?si=3xU5rA7_6TXuJssU" target="_blank" rel="noopener">Video (YouTube)</a>
</div>

> **Note**
> - `Paper (temp)` 버튼은 현재 `static/paper.pdf`를 가리키도록 해뒀어. 나중에 PDF를 그 경로에 넣거나 링크를 arXiv로 바꾸면 돼.
> - YouTube 영상은 위 링크로 연결되도록 설정 완료.

---

## Teaser (Temporary)

![Teaser](static/image/teaser.png)

<p style="margin-top:6px; color:#666;">
  (Temporary teaser image) Replace <code>static/image/teaser.png</code> with your teaser.
</p>

---

## Abstract

We present **GRAPE (Gaussian Rendering for Accelerated Pixel Enhancement)**, a fast, lightweight method for **arbitrary-scale super-resolution (ASSR)** based on **2D Gaussian splatting**. GRAPE predicts anisotropic Gaussian parameters (RGB, rotation, scale, offset) with a compact point-wise layer, and renders the high-resolution image in **one pass** via a differentiable rasterizer. The full model has **1.56M parameters**, uses **1.10GB** GPU memory, and reaches **69.33 FPS on Urban100 at ×4** (average 985×798), reporting over **315×** speed-up compared to GSASR while maintaining competitive quality.

---

## Method

### Overview

GRAPE is an end-to-end differentiable pipeline:

1. **Encoder** extracts LR features.  
2. **Gaussian Head (1×1 point-wise)** maps features to anisotropic 2D Gaussian parameters (RGB / rotation / scale / offset).  
3. **2D Rasterizer** renders the SR image efficiently in a single pass.

![Method Overview (Temporary)](static/image/method.png)

<p style="margin-top:6px; color:#666;">
  (Temporary) Replace <code>static/image/method.png</code> with your method overview figure.
</p>

---

## Results

### Quantitative (Temporary)

![Quantitative Table (Temporary)](static/image/table.png)

<p style="margin-top:6px; color:#666;">
  (Temporary) Replace <code>static/image/table.png</code> with your quantitative results table/plot.
</p>

### Speed / Efficiency Highlights

- **Params:** 1.56M  
- **Memory:** 1.10 GB  
- **Speed:** 69.33 FPS (Urban100, ×4, avg 985×798)

> Replace these bullets with your final reported numbers if you want the project page to exactly match the paper.

---

### Qualitative (Temporary)

<div style="display:grid; grid-template-columns: repeat(2, 1fr); gap:12px; margin-top:12px;">
  <img src="static/image/qual_1.png" alt="Qualitative 1" style="width:100%; border-radius:12px;" />
  <img src="static/image/qual_2.png" alt="Qualitative 2" style="width:100%; border-radius:12px;" />
  <img src="static/image/qual_3.png" alt="Qualitative 3" style="width:100%; border-radius:12px;" />
  <img src="static/image/qual_4.png" alt="Qualitative 4" style="width:100%; border-radius:12px;" />
</div>

<p style="margin-top:6px; color:#666;">
  (Temporary) Replace <code>qual_1.png ~ qual_4.png</code> with qualitative comparison images.
</p>

---

## Video

<div style="position:relative;padding-top:56.25%; margin-top:12px;">
  <iframe
    style="position:absolute;top:0;left:0;width:100%;height:100%; border:0;"
    src="https://www.youtube.com/embed/LwlF6hZ54ng"
    title="GRAPE Demo Video"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen>
  </iframe>
</div>

---

## BibTeX (Temporary)

```bibtex
@article{grape2025,
  title   = {GRAPE: Gaussian Rendering for Accelerated Pixel Enhancement},
  author  = {Jang, Jung In and Jin, Kyong Hwan},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},
  year    = {2025}
}
