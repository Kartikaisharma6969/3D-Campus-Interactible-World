# 🏛️ 3D Interactive Campus Simulation & Open-World Environment

[![Engine](https://img.shields.io/badge/Engine-Unreal%20Engine%205-eceff4?style=flat-square&logo=unrealengine&logoColor=white&color=0e1128)](https://unrealengine.com)
[![Tools](https://img.shields.io/badge/3D%20Modeling-Blender-eceff4?style=flat-square&logo=blender&logoColor=white&color=ea7638)](https://blender.org)
[![Version Control](https://img.shields.io/badge/Version%20Control-Diversion-eceff4?style=flat-square&color=3b82f6)](https://diversion.dev)

A real-time, fully interactive 3D simulation and digital twin of the **Shri Vishnu SD Post Graduate College Bhatoli** campus. Built from scratch as a seamless open-world experience, this project bridges the gap between vast exterior landscapes and highly detailed structural interiors.

---

## 🚀 Project Overview

This environment features true continuous exploration from "mountain-to-mountain" regional terrain directly down into specific building corridors, individual floors, pillars, and classrooms with zero loading screens. 

The primary development challenge was managing a massive scene containing **over 150,000 unique objects** while maintaining stable, smooth performance on mid-range target hardware.

---

## 🛠️ Tech Stack & Workflow

*   **Game Engine:** Unreal Engine 5 (UE5)
*   **3D Modeling & Asset Pipeline:** Blender
*   **Collaborative Version Control:** **Diversion** (Maintained a robust workflow with 220+ commits over an intensive 2-month development sprint)

### The Modular Pipeline
Every structural element—including walls, ceilings, floors, corridors, pillars, and precise window/door gaps—was meticulously modeled as modular assets within Blender before being imported and systematically assembled inside Unreal Engine 5.

---

## ⚡ Technical Challenges & Optimization (Target: 8GB RAM / 4GB VRAM)

To prevent severe GPU draw-call bottlenecks and excessive memory allocation, aggressive engine-level optimization workflows were deployed:

*   **Hierarchical Instanced Static Meshes (HISM):** Thousands of repetitive assets (such as structural pillars, windows, and environmental foliage) were converted into HISMs, collapsing massive rendering overhead into single-pass GPU draw calls.
*   **World Partition System:** Leveraged UE5's World Partitioning to dynamically stream terrain grid cells in and out of active runtime memory based on player proximity.
*   **Foliage & LOD Tuning:** Handled heavy regional vegetation using tight Level of Detail (LOD) transitions and aggressive per-instance fade distances to safeguard frame stability.

---

## 👥 Team & Collaboration

This project was co-developed by a dedicated 2-person development team. We used a strict branch-and-commit workflow via Diversion to seamlessly coordinate asset integration, technical layout assembly, landscape painting, and performance profiling.

---

## 🔧 Getting Started

1. Clone this repository.
2. Ensure you have **Unreal Engine 5.x** installed.
3. Open `CampusSimulation.uproject`.
4. *Note:* Source asset files (`.blend`) are organized within the `_SourceAssets/` directory.
