# 1141ML Final Project  
## Reconstructing Ancient Life through Molecular Diffusion Models  
_313652018 王宣瑋_

This repository contains the implementation, experiments, and results for the 
final project of 1141 Machine Learning (Winter 2025).
The goal is to explore diffusion-based generative models through simplified toy 
problems, and investigate their potential applications in reconstructing ancient 
molecular structures.

---

## 📌 Project Structure
├── code/ # Jupyter notebooks and training scripts

├── report/ # Final LaTeX report source

└── README.md


---

## 🔍 1. Motivation

- Understand the forward–reverse paradigm of diffusion models.  
- Study DSM (denoising score matching) as the foundation of GEODIFF, RFdiffusion, and EDM.  
- Observe whether score-based models can recover structured data distributions.  
- Connect toy reconstruction tasks to future molecular reconstruction goals.

---

## 🧪 2. Methods Overview

### **Denoising Score Matching (DSM)**  
- Learn an approximation of the score function:
  $$s_\theta(x) \approx \nabla_x \log p(x)$$
- Reverse noise corruption using Langevin dynamics:
  $$x_{k+1} = x_k + \eta\, s_\theta(x_k) + \sqrt{2\eta}\, z_k$$
  

### **Datasets**
- 1D Gaussian mixture  
- 2D Gaussian blobs  
- 2D blob + noisy line mixture  

### **Training Setup**
- Optimizer: Adam  
- Noise levels vary by dataset  
- Hardware: CPU  

---

## 📈 3. Experimental Results

- Training loss curves (1D and 2D)  
- Forward–Backward reconstruction $(p_0 → p_T → p_0′)$  
- 2D reconstruction performance  
- Discussion on variance expansion, mode recovery, and geometry deformation  

All figures are stored in ```report```

---

## 🧠 4. Discussion

- DSM effectively reconstructs multimodal distributions.  
- Performance decreases for anisotropic or non-Gaussian structures.  
- Reveals challenges when scaling DSM to molecular-level geometry.  

---

## 📜 5. Report

The complete LaTeX report is located in ```report```

---

## 🧭 6. Future Work

- Multi-σ DSM, NCSN++, or EDM  
- Implement full DDPM/score-based models  
- Apply diffusion models on geometric or molecular data structures  

---

## 👤 Author

- **Student:** 313652018 王宣瑋
- **Course:** 1141 Machine Learning (Winter 2025)  

## Acknowledgement
Some portions of the writing were refined using AI-assisted language tools to improve clarity. 
All technical content, analysis, and experimental design were produced by the author.
