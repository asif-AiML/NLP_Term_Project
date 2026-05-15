# Parameter-Efficient NLP for Edge Computing: CURA vs 1D-CNN

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview
This repository contains the code, trained weights, and interactive results for the evaluation of the **Compact Universal Architecture (CURA)** against a baseline **1D-CNN** for text classification. 

Designed specifically for resource-constrained IoT and edge computing environments, this research demonstrates how temporal gating mechanisms (CURA) can replace brute-force spatial convolutions (1D-CNNs). The CURA model achieves a **99.25% reduction in parameter volume** (from 835k to 6k parameters) and a **31.3% acceleration in CPU inference latency**, while maintaining highly competitive predictive fidelity (0.944 F1-Score) on a highly imbalanced dataset.

## Dataset
This project utilizes the __Yelp Open Dataset__ (approx. 3.6 million samples).
**Note:** Due to GitHub's file size constraints, the raw data files (5GB JSON / 2GB CSV) are not included in this repository.

To reproduce the experiments, please run the notebook located at CODEBASE/YELP_OPEN_DATASET.ipynb. This script will automatically download the raw JSON, extract the relevant review text and metadata, and prepare the formatted CSV required for training.

## Installation & Setup
To run this project locally, clone the repository and install the required dependencies.
*git clone [https://github.com/asif-AiML/NLP_Term_Project.git](https://github.com/asif-AiML/NLP_Term_Project.git)
cd NLP_Term_Project
pip install -r requirements.txt*
(Note: Ensure you are using a virtual environment).

## Usage
1. Prepare the Data: Run YELP_OPEN_DATASET.ipynb to generate the training and testing CSVs.
2. Load Dataset & Train: Run CURA_vs_CNN.ipynb to load the dataset, apply tokenization and starts training.
3. View Interactive Results: Open the Results/  folder directly in any web browser to view the interactive Pareto efficiency and loss convergence plots.

## Author
__Muhammad Asif__
Master's Research Project | Edge Computing & Deep Learning Architectures

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
