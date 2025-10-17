# Deep Learning for Cortical Surface Reconstruction — OHBM Posters (2023 & 2024)

This repo contains two OHBM posters on fast, accurate cortical surface reconstruction with modern deep learning.  
The 2023 poster is a head-to-head benchmark study (the **Takeaway** poster). The 2024 poster extends **PialNN** with a Graph Neural Network (**PialGCN**) that performed strongly on pial surfaces.

---

## Quick links

- **OHBM 2023 — Benchmarks & Takeaway (PDF)**  
  https://github.com/WilliamAshbee/OHBM_posters/blob/69253b2a69cf2b49586f7577e311d22a372c99d1/OHBM_2023.pdf
- **OHBM 2024 — PialGCN (PDF)**  
  https://github.com/WilliamAshbee/OHBM_posters/blob/69253b2a69cf2b49586f7577e311d22a372c99d1/OHBM_2024.pdf

---

## TL;DR (from the 2023 poster)

- **All deep learning methods are faster than FreeSurfer**, but **few fully match its accuracy**.
- The **medial wall** is the most defect-prone region (topology/self-intersections).
- Qualitative distance maps localize failure modes across methods.

---

## What’s in the 2023 poster

### Models compared
CorticalFlow++, CortexODE, DeepCSR, PialNN, TopoFit, Vox2Cortex, with FreeSurfer as reference.

### Metrics & visuals
- **Hausdorff distance heatmaps** for *pial* and *white* surfaces vs. FreeSurfer  
  (shared color scale; values > 1 are binned as outliers; in the legend: **red = good, blue = bad**).
- **Runtime / memory / model size** comparisons (load and inference time, GPU peak memory, model MB).
- **Topology**: self-intersection counts highlighting regional fragility (notably the medial wall).

---

## OHBM 2024 — PialGCN (Graph extension to PialNN)

- **Idea:** enrich PialNN with **graph convolutions** to use neighborhood context for vertex updates.  
- **Outcome:** improved pial surface quality while keeping memory use practical.  
- **Stack:** PyTorch / PyTorch Geometric (mesh-aware ops), standard vertex-wise losses (e.g., MSE; Chamfer for validation).  
- **Note:** this work complements the 2023 benchmarks by showing how lightweight GNN layers can close accuracy gaps on pial surfaces.

---

## Relation to the review

These posters pair with my survey on deep-learning-based cortical surface reconstruction, emphasizing:
- trade-offs between **speed** and **accuracy**,
- architectural choices across flow/ODE/mesh-GNN approaches, and
- where/why models fail (heatmaps + topology).

---

## Cite

If you use figures, ideas, or comparisons from these posters, please cite:

- **OHBM 2023 Poster:** *Surface Reconstruction for the Masses: Benchmarking Modern Deep Learning Models* (Poster).  
- **OHBM 2024 Poster:** *PialGCN: A Graph-Neural Extension to PialNN for Cortical Surfaces* (Poster).

---

## Contact

**William Ashbee** — wsashbee@gmail.com
