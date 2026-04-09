# AM4D-Fusion: A 4D Multimodal Dataset for Predictive Industrial Defect Analysis

## Overview

AM4D-Fusion is a large-scale 4D (3D + time) multimodal dataset for industrial defect analysis. It is designed to support research on temporal defect detection, defect evolution modeling, and early failure prediction in advanced manufacturing scenarios such as hybrid laser–MIG welding and additive manufacturing.

Unlike conventional industrial datasets that rely on static snapshots or single-modality observations, AM4D-Fusion contains synchronized RGB, thermal, and point cloud sequences, together with annotations that track defect evolution over time. The dataset is intended to help researchers study defects as spatio-temporal and cross-modal phenomena rather than isolated events.

## Dataset Generation Process

AM4D-Fusion was constructed from synchronized multimodal sensing and numerical simulation.

### 1. Multimodal acquisition
A synchronized multi-sensor rig was deployed to capture:
- **RGB-V**: high-resolution RGB video
- **Thermal-T**: long-wave infrared thermal imaging
- **Geometric-P**: structured-light 3D point cloud data

The three modalities were temporally aligned and spatially calibrated to support cross-modal analysis.

### 2. Sequence construction
Each sample is organized as a time-ordered multimodal sequence, allowing the defect formation process to be studied across:
- pre-defect stage
- onset stage
- growth stage
- failure stage

### 3. Annotation
Annotations were created at multiple levels:
- **Frame-level labels**: defect / normal, category labels, and localization annotations
- **Temporal labels**: defect onset, peak, and failure times
- **Cross-modal correspondence**: synchronized RGB, thermal, and point cloud alignment

### 4. Benchmark task preparation
The dataset is organized to support three benchmark tasks:
1. **Temporal defect detection**
2. **Defect evolution modeling**
3. **Early failure prediction**

## Dataset Statistics

- **Number of sequences**: 1,200
- **Total frames**: 2.4 million
- **Total duration**: 160 hours
- **Frame rate**: 10–30 fps, synchronized at 10 Hz
- **Annotated defect instances**: 8,500+
- **Machines / conditions**: 12 machines across 35 process conditions

### Resolution by modality
- **RGB**: 1920 × 1080
- **Thermal**: 640 × 512
- **Point cloud**: ~100k points per frame

## Dataset Structure

A typical sample is organized as follows:

```text
AM4D-Fusion/
├── train/
├── val/
├── test/
├── annotations/
├── rgb/
├── thermal/
├── pointcloud/
├── splits/
└── baselines/
