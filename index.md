---
layout: project_page
permalink: /

title: "GRAPE(Gaussian Rendering for Accelerated Pixel Enhancement) Brings Fast
and Lightweight Arbitrary Super-Resolution"
authors:
  Jung In Jang¹ · Kyong Hwan Jin¹
affiliations:
  ¹Korea University, Republic of Korea
paper: static/paper.pdf
video: https://youtu.be/LwlF6hZ54ng
code: https://github.com/mulkkog/GRAPE 
---
 

## Abstract

GRAPE enables **arbitrary-scale super-resolution (ASSR)** by predicting **2D anisotropic Gaussian primitives** on an image-space grid and efficiently rasterizing them into high-resolution outputs.

Instead of using heavy decoder architectures, GRAPE adopts a **single-layer Gaussian prediction head** combined with a **GPU-friendly splatting renderer**. This design enables fast, cache-efficient, and highly parallel inference at arbitrary output resolutions.

With only **1.56M parameters** and **1.10 GB peak GPU memory**, GRAPE achieves **69.33 FPS on Urban100 (985×798)** while maintaining high reconstruction fidelity.

---

## Method
GRAPE is an end-to-end differentiable pipeline:

1. **Encoder** extracts low-resolution feature maps  
2. **Feature Reshaping & Parameter Mapping** converts features into a structured grid representation  
3. **Gaussian Head (Point-wise Prediction)** predicts anisotropic 2D Gaussian parameters:
   - RGB color
   - Rotation
   - Scale
   - Spatial offset  
4. **2D Rasterizer** composites Gaussian primitives into the final high-resolution image in a single rendering pass  

![Method Overview](/static/image/method.png)

---

## 2D Anisotropic Gaussian Splatting
Oriented elliptical Gaussian footprints align naturally with edges and directional textures, improving structural fidelity and fine-detail reconstruction.

Below are visualizations of learned anisotropic parameters such as scale and rotation-related maps.

![Anisotropic Visualization](/static/image/ani.png)

---

## Results

### Qualitative Results (Urban100 Examples)
![Qualitative Results](/static/image/qual.png)

### Quantitative Results
The following tables summarize quantitative comparisons across benchmark datasets.

![Table 1](/static/image/table1.png)  
![Table 2](/static/image/table2.png)  
![Table 3](/static/image/table3.png)

---

## Runtime and Memory Efficiency
GRAPE reconstructs a Full-HD frame in **40.88 ms**.  
The encoder accounts for approximately **85.1% of total runtime**, while the Gaussian head and rasterizer introduce minimal overhead.

Peak GPU memory usage remains below **2.12 GB**, demonstrating strong efficiency for high-resolution inference.

![Peak GPU Memory and Latency](/static/image/peak_gpu.png)

---
 
## Citation
```bibtex
@article{grape2025,
  title   = {GRAPE: Gaussian Rendering for Accelerated Pixel Enhancement},
  author  = {Jang, Jung In and Jin, Kyong Hwan},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},
  year    = {2025}
}
```

## Acknowledgements

This project page is adapted from the original project website template by:
https://github.com/shunzh/project_website and customized for GRAPE.   
