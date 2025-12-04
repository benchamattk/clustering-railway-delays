# Railway Delay Clustering

This repository contains the research code and analysis for a study on clustering railway delay incidents,
submitted to *IEEE BigData 2025 – Industry & Government Track*.

---

## Overview

This project investigates patterns of railway delay incidents using clustering techniques on mixed-type data.
The objective is to identify station-level operational patterns by jointly analyzing numerical and categorical features from open government datasets.

The study applies **K-Prototypes clustering** for mixed-type data and benchmarks its performance against two
alternative methods:

- K-Means with one-hot encoding  
- Agglomerative clustering using Gower distance  

The results show how incorporating categorical attributes (e.g., cause types, time-of-day categories,
and calendar effects) enables insights that are not accessible through numerical-only clustering approaches.

---

## Methodology

The analysis workflow includes:

- Data cleaning and validation  
- Data integration of passenger volume and incident records  
- Feature engineering for:
  - time-of-day categories  
  - weekend and public-holiday flags  
  - intermodal connectivity indicators  
- Clustering analysis using three methods for comparison  
- Evaluation using Silhouette scores (computed via Gower distance)  
- Cluster profiling and interpretation  

---

## Repository Structure

```text
railway-delay-clustering/
│
├── notebooks/
│   └── railway_delay_clustering_analysis.ipynb
│
├── data/
│   ├── passenger_volume.csv
│   └── incident_data.csv
│
├── README.md
└── LICENSE
