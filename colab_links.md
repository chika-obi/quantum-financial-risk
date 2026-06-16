# One-Click Colab Links

Click the links below to open each notebook directly in Google Colab.

| Notebook | Description | Colab Link |
|----------|-------------|------------|
| 01_data_preparation | Download S&P 500 data, create features, train/test split | [Open in Colab](https://colab.research.google.com/github/chika-obi/quantum-financial-risk/blob/main/notebooks/01_data_preparation.ipynb) |
| 02_classical_baseline | Train Ridge Regression, Random Forest, XGBoost, Neural Network | [Open in Colab](https://colab.research.google.com/github/chika-obi/quantum-financial-risk/blob/main/notebooks/02_classical_baseline.ipynb) |
| 03_lstm_baseline | Train LSTM deep learning model | [Open in Colab](https://colab.research.google.com/github/chika-obi/quantum-financial-risk/blob/main/notebooks/03_lstm_baseline.ipynb) |
| 04_risk_metrics | Calculate VaR and CVaR at 95% and 99% confidence | [Open in Colab](https://colab.research.google.com/github/chika-obi/quantum-financial-risk/blob/main/notebooks/04_risk_metrics.ipynb) |
| 05_results_visualization | Generate publication-ready figures | [Open in Colab](https://colab.research.google.com/github/chika-obi/quantum-financial-risk/blob/main/notebooks/05_results_visualization.ipynb) |

---

## Instructions

1. Click the **"Open in Colab"** link for the notebook you want to run.
2. When Colab opens, click **"Copy to Drive"** (this saves your own editable copy).
3. Go to **Runtime → Run all** to execute the entire notebook.

## Recommended Order

Run the notebooks in this order:

1. **01_data_preparation** - Prepares the data (run once)
2. **02_classical_baseline** - Trains classical models
3. **03_lstm_baseline** - Trains LSTM model
4. **04_risk_metrics** - Calculates risk metrics
5. **05_results_visualization** - Generates final figures

## Notes

- These notebooks use **real S&P 500 data** from Yahoo Finance (2020-2024).
- All results are **reproducible** - run them yourself to verify.
- The code is **open source** under the MIT License.
- If you encounter errors, check that you have the latest versions of libraries (`pip install -r requirements.txt`).

## Citation

If you use this code in your research, please cite:

```bibtex
@software{Kpanuku_Quantum_Financial_Risk_2025,
  author = {Kpanuku, Chika-Obi},
  title = {Predicting Financial Risk: Benchmarking Classical Models and Exploring Quantum Neural Networks on S&P 500 Data},
  year = {2025},
  url = {https://github.com/chika-obi/quantum-financial-risk}
}