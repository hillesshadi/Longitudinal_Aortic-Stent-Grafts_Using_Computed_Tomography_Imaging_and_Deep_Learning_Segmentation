# Automated Longitudinal Pipeline for Aortic Stent-Graft AnalysisProject 
## Overview
This repository hosts a comprehensive computational pipeline designed for the automated longitudinal analysis of aortic stent-grafts using CT imaging. Developed within a deep learning framework (nnU-Net), the workflow enables precise tracking of device positioning and displacement over multiple post-EVAR (Endovascular Aneurysm Repair) surveillance intervals.
## Key Features
### Automated Segmentation: 
Implementation of a dual-structure segmentation pipeline for the aorta and intimal flaps/stents.
### Advanced Preprocessing: 
Integration of image enhancement evaluation and denoising protocols.
### Displacement Quantification: 
A centroid-based analytical engine that calculates spatial divergence and directional migration trajectories ($x, y, z$ coordinates).
### 3D Visualization: 
A clinically interpretable visualization framework using PyVista, providing geometrically grounded 3D representations of temporal device displacement.
### Multi-Metric Validation: 
Rigorous evaluation using Dice Similarity Coefficient (DSC), Hausdorff Distance (HD95), and cross-dataset spatial overlap analysis.
## Current Research Findings
In its current iteration, the study identifies critical challenges in automated post-EVAR surveillance:
### Performance Metrics: 
Current segmentation performance (DSC: 0.0824–0.2273) highlights the impact of training data scarcity and metallic beam-hardening artifacts typical in single-patient longitudinal studies.
### Migration Patterns: 
Despite artifact limitations, the pipeline successfully characterized progressive stent-graft positional divergence. Results showed a decline in cross-dataset DSC (0.1004 to 0.0076) and a craniocaudally dominant displacement consistent with established clinical migration patterns.
### Clinical Utility: 
The 3D visualization framework meaningfully augments standard radiological reviews by providing a spatial context that 2D slices cannot offer.
## Technical Stack
### Framework: 
nnU-Net (Deep Learning Segmentation)
### Processing: 
Python, SimpleITK, Nibabel, Pydicom
### Visualization: 
PyVista (3D), Matplotlib (2D)
### Data Handling: 
Excel-based quantification of longitudinal displacement values.
## Roadmap for Clinical Translation
To bridge the gap to clinical-grade accuracy, future development focuses on:
### Multi-centre Dataset Expansion 
to improve model generalization.
### Metal Artifact Reduction (MAR) 
algorithms to mitigate beam-hardening effects.
### Deformable Image Registration 
to enhance longitudinal tracking precision.
