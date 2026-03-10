# 3D Scene Reconstruction from RGB-D Images

This project implements a computer vision pipeline for reconstructing 3D scenes from RGB-D image sequences.  
The system generates point clouds from RGB and depth images and integrates them into a reconstructed 3D environment.

This project explores modern 3D reconstruction methods using **DUSt3R**, **Fast3R**, and transformer-based pose refinement.

---

# Project Overview

3D scene reconstruction is an important task in computer vision and robotics, enabling machines to understand spatial structures from visual observations.

In this project, we reconstruct 3D scenes from RGB-D images using a multi-stage pipeline that includes:

- RGB-D image processing
- camera pose estimation
- point cloud generation
- 3D reconstruction
- evaluation using accuracy and completeness metrics

The project uses the **7Scenes dataset**, a widely used dataset for indoor scene reconstruction.

---

# Pipeline

RGB Image + Depth Image  
↓  
Pose Estimation (DUSt3R / Fast3R)  
↓  
Pose Refinement (Transformer)  
↓  
Point Cloud Generation  
↓  
Point Cloud Integration  
↓  
3D Scene Reconstruction  

---

# Methods

### 1. Direct Reconstruction

Generate point clouds directly from RGB-D images and ground truth poses.

Accuracy = 0.0  
Completeness = 0.51

---

### 2. DUSt3R Pose Estimation

Use **DUSt3R** to estimate camera poses and reconstruct the scene.

Accuracy = 0.18  
Completeness = 0.05

---

### 3. Fast3R + Transformer Refinement

Use **Fast3R** for pose prediction and apply a transformer-based model to refine camera poses.

Accuracy = 0.16  
Completeness = 0.10

---

# Dataset

This project uses the **Microsoft 7Scenes dataset**, which contains RGB images, depth images, and camera pose annotations.

Dataset structure example:
