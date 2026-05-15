# Parameter-Efficient NLP for Edge Computing: CURA vs 1D-CNN

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview
This repository contains the code, trained weights, and interactive results for the evaluation of the **Compact Universal Architecture (CURA)** against a baseline **1D-CNN** for text classification. 

Designed specifically for resource-constrained IoT and edge computing environments, this research demonstrates how temporal gating mechanisms (CURA) can replace brute-force spatial convolutions (1D-CNNs). The CURA model achieves a **99.25% reduction in parameter volume** (from 835k to 6k parameters) and a **31.3% acceleration in CPU inference latency**, while maintaining highly competitive predictive fidelity (0.944 F1-Score) on a highly imbalanced dataset.

## Repository Structure
The project is encapsulated within the `NLP_Term_Project` directory to maintain dependency links between the notebooks, weights, and interactive plots.

```text
NLP_Term_Project/
│
├── CODEBASE/
│   └── YELP_OPEN_DATASET.ipynb   # Notebook to fetch and process raw data
│   └── CURA_vs_CNN.ipynb   # Notebook contain the code including models implementation code, training and evalution
│
├── Results/                      # Interactive Plotly visualizations
│   
│ 
│
├── Trained_weights/                        
│   ├── 1D-CNN_RAW_YELP_Weights.pth
│   └── CURA_RAW_YELP_WEIGHTS.pth
│
└── README.md
