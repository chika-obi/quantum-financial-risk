# Predicting Financial Risk: Benchmarking Classical Models and Exploring Quantum Neural Networks on S&P 500 Data

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

## 📌 Overview

This repository contains the complete code and results for my research on financial risk prediction. I compared six machine learning models to see which one predicts daily S&P 500 returns best. The models tested were:

- Ridge Regression
- Random Forest
- Gradient Boosting
- XGBoost
- Neural Network
- LSTM (Long Short-Term Memory)

I also explored Quantum Neural Networks (QNN) and documented the challenges encountered.

## 🏆 Key Results

| Model | Test RMSE (%) |
|-------|---------------|
| **Ridge Regression** | **0.818** |
| LSTM | 0.822 |
| Neural Network | 0.834 |
| Gradient Boosting | 0.835 |
| Random Forest | 0.857 |
| XGBoost | 0.961 |

### Risk Metrics (Ridge Regression)

| Metric | Value |
|--------|-------|
| VaR 95% | -1.21% |
| CVaR 95% | -1.57% |
| VaR 99% | -1.94% |
| CVaR 99% | -2.28% |

**Main takeaway:** A simple linear model with regularization (Ridge Regression) performed as well as complex deep learning models. Start simple.

## 📁 Repository Structure
quantum-financial-risk/
├── notebooks/ # All Jupyter notebooks (run in order)
├── results/ # Figures, JSON results, and tables
├── paper/ # LaTeX source for the paper
├── requirements.txt # Python dependencies
├── colab_links.md # One-click links to open notebooks in Colab
└── README.md # This file

## 🚀 Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/chika-obi/quantum-financial-risk.git
cd quantum-financial-risk

### 2. Install dependencies
pip install -r requirements.txt

### 3. Run notebooks in order
Notebook	Description
01_data_preparation.ipynb	Download S&P 500 data, create features
02_classical_baseline.ipynb	Train Ridge, RF, XGBoost, NN
03_lstm_baseline.ipynb	Train LSTM model
04_risk_metrics.ipynb	Calculate VaR and CVaR
05_results_visualization.ipynb	Generate all figures

4. One-click Colab links
Open any notebook directly in Google Colab via colab_links.md

📊 What Each Notebook Does
01_data_preparation: Downloads S&P 500 data (2020-2024), creates 6 features (5 lagged returns + rolling volatility), normalizes, and splits into train/test

02_classical_baseline: Trains and evaluates all classical models, saves results to JSON

03_lstm_baseline: Builds a 2-layer LSTM with dropout, trains with early stopping

04_risk_metrics: Calculates VaR and CVaR at 95% and 99% confidence levels

05_results_visualization: Creates publication-ready figures (bar charts, heatmaps, scatter plots)

📈 Results Summary
Ridge Regression achieved the lowest test RMSE at 0.818 percent. LSTM followed closely at 0.822 percent. The difference is small enough that both models are practically equivalent for risk prediction.

For risk managers, Ridge Regression estimates:

A 5% chance of prediction error exceeding 1.21% (VaR 95%)

When losses exceed that, the average loss is 1.57% (CVaR 95%)

A 1% chance of error exceeding 1.94% (VaR 99%)

In extreme cases, average loss is 2.28% (CVaR 99%)

⚠️ Quantum Neural Network Attempt
I also attempted to build a Quantum Neural Network using PennyLane with 2 qubits and 2 variational layers. Training failed immediately due to gradient stability issues (NaN losses from epoch zero). This is documented in the paper as a lesson learned. Quantum machine learning for finance remains promising but needs more stable frameworks.

📝 Citation
If you use this code or results in your research, please cite:

bibtex
@software{Kpanuku_Quantum_Financial_Risk_2025,
  author = {Kpanuku, Chika-Obi},
  title = {Predicting Financial Risk: Benchmarking Classical Models and Exploring Quantum Neural Networks on S&P 500 Data},
  year = {2025},
  url = {https://github.com/chika-obi/quantum-financial-risk}
}
📧 Contact
Author: Kpanuku Chika-Obi
Email: chikaobi.kpanuku@rsu.edu.ng
Department: Computer Science, Rivers State University, Port Harcourt, Nigeria

📜 License
Distributed under the MIT License. See LICENSE file for more information.

text

---

## How to Update Your README on GitHub

### Method 1: Directly on GitHub Website

1. Go to your repository: `https://github.com/chika-obi/quantum-financial-risk`
2. Find `README.md` in the file list
3. Click on it to open the file
4. Click the pencil icon (✏️) in the top right corner of the file view
5. Delete all existing text
6. Copy and paste the new README content from above
7. Scroll down and click **"Commit changes"**

### Method 2: Upload from Colab

```python
# Create the new README file in Colab
readme_content = '''# Paste the entire README content from above here'''

with open('README.md', 'w') as f:
    f.write(readme_content)

# Push to GitHub
!git add README.md
!git commit -m "Update README with classical model results"
!git push origin main

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20615223.svg)](https://doi.org/10.5281/zenodo.20615223)