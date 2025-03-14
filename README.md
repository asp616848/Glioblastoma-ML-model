# Multi-View Learning for Addressing Unbalanced/Partial Data Modalities in Glioblastoma Survival Prediction

## Overview
Glioblastoma (GBM) is an aggressive form of brain tumor with a poor prognosis. Accurate survival prediction is crucial for personalized treatment planning. Our study leverages multi-modal learning techniques to handle missing or unbalanced data modalities in Glioblastoma survival prediction.

## Motivation
Survival prediction in Glioblastoma patients is challenging due to:
- **Heterogeneous data**: Imaging, pathology, molecular, and clinical features vary across patients.
- **Missing modalities**: Not all patients have complete data, making traditional deep learning models unreliable.
- **Interpretability issues**: Black-box models lack transparency, reducing their adoption in clinical settings.

## Approach
We propose a **multi-view learning framework** that integrates incomplete data modalities to enhance survival prediction. Our methodology includes:
- Data preprocessing and feature extraction across MRI, histopathology, and clinical data.
- Multi-modal deep learning models trained on incomplete data.
- Interpretability techniques for model transparency and clinical trust.

## Data Sources
We utilized publicly available datasets from **The Cancer Imaging Archive (TCIA)**:

- **MRI & Radiomic Data**: [Download (69GB, 630 participants, 10645 files in NIfTI format)](https://faspex.cancerimagingarchive.net/aspera/faspex/public/package?context=eyJyZXNvdXJjZSI6InBhY2thZ2VzIiwidHlwZSI6ImV4dGVybmFsX2Rvd25sb2FkX3BhY2thZ2UiLCJpZCI6IjYwNCIsInBhc3Njb2RlIjoiYzJiMjI2Mzg5ZjljYWE0NWNkYjc4MzM4NWE4Yzc2MjBjNGU1NDY1MiIsInBhY2thZ2VfaWQiOiI2MDQiLCJlbWFpbCI6ImhlbHBAY2FuY2VyaW1hZ2luZ2FyY2hpdmUubmV0In0=&redirected=true)
  - Includes MRI scans, segmented tumor images, and radiomic features.
  - Additional details: [DOI Link](https://doi.org/10.7937/TCIA.709X-DN49)

- **Histopathology Images**: [Download (34 patients, 71 images)](https://faspex.cancerimagingarchive.net/aspera/faspex/public/package?context=eyJyZXNvdXJjZSI6InBhY2thZ2VzIiwidHlwZSI6ImV4dGVybmFsX2Rvd25sb2FkX3BhY2thZ2UiLCJpZCI6IjkzOCIsInBhc3Njb2RlIjoiZGU4NmU1NDViMzExZTczMmU4YjVmYTQyNzlkZGYyNjUzOGY1MWY1NSIsInBhY2thZ2VfaWQiOiI5MzgiLCJlbWFpbCI6ImhlbHBAY2FuY2VyaW1hZ2luZ2FyY2hpdmUubmV0In0=&redirected=true)
  - Multi-parametric MRI scans from **UPENN-GBM collection**.
  - More details: [DOI Link](https://doi.org/10.7937/TCIA.709X-DN49)

## Methods
### Data Preprocessing
- Converted **DICOM** to **NIfTI** for MRI images.
- Extracted tumor-specific features using radiomics principles.
- Tiled histopathology images into smaller patches to improve computational efficiency.
- Performed **Exploratory Data Analysis (EDA)** on clinical data, handling missing values and feature correlations.

## Results & Findings
- The multi-view model performed better than single-modality models in survival prediction.
- The interpretability approach helped identify key biomarkers for prognosis.
- Future work includes expanding datasets and improving generalization.

## Research References
Our work is supported by recent research papers:
1. [Glioblastoma: An Update in Pathology, Molecular Mechanisms and Biomarkers](https://academic.oup.com/noa/article/6/1/vdae122/7712392)
2. [Epidemiology of Glioblastoma Multiforme](https://pubmed.ncbi.nlm.nih.gov/39156618/)
3. [Survival Prediction using Machine Learning & Deep Learning](https://pmc.ncbi.nlm.nih.gov/articles/PMC10522528/)
4. [MRI-Based Survival Analysis](https://bmccancer.biomedcentral.com/articles/10.1186/s12885-024-13320-4#citeas)

