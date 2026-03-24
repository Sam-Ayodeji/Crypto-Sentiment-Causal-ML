# Causal Effects of Social Media Sentiment on Cryptocurrency Returns and Volatility

## Double ML · IV-DML · Causal Forest | Bitcoin & Ethereum | January – June 2023

This repository contains the full code and data for the study investigating the causal impact of social media sentiment on cryptocurrency returns and volatility, focusing on Bitcoin and Ethereum during the first half of 2023.

The study employs advanced causal inference techniques, including Double Machine Learning (DML) with partial linear regression (PLR), Instrumental Variable DML (IV-DML), and Causal Forests, to robustly estimate treatment effects and explore heterogeneity.

## Table of Contents
- [Overview]
- [Data Sources]
- [Setup and Installation](#setup-and-installation)
- [Running the Notebook
- [Key Findings
- License

## Overview

The `Causal_ML_Sentiment_Crypto_Clean.ipynb` notebook implements the entire analysis pipeline:
1.  **Data Loading & Preprocessing**: Ingesting CoinMarketCap and Crypto Twitter Influencer datasets, followed by merging and feature engineering.
2.  **Preliminary Analysis & Suitability Tests**: Ten diagnostic tests (e.g., normality, stationarity, multicollinearity, Granger causality, Hausman endogeneity, overlap checks) to validate data assumptions for DML and Causal Forests.
3.  **Causal ML Pipeline**: Application of OLS (baseline), DML-PLR, IV-DML (for endogenous treatments), and Causal Forest for estimating Average Treatment Effects (ATEs) and Conditional Average Treatment Effects (CATEs).
4.  **Robustness Checks**: Six families of robustness tests to ensure the stability and validity of the primary causal estimates.

## Data Sources

The datasets used in this study are publicly available:
-   **CoinMarketCap**: Daily OHLCV data for cryptocurrencies.
    -   *Citation*: Damaševičius (2025), Zenodo: 10.5281/zenodo.14749166
-   **Crypto Twitter Influencer**: VADER sentiment scores, importance coefficients, and engagement metrics from Twitter.
    -   *Citation*: Jahanbin et al. (2023), Mendeley: 10.17632/8fbdhh72gs.5

*Note: The datasets are downloaded programmatically within the notebook.*

## Setup and Installation

To run this analysis, you will need a Python environment with the required libraries. It is recommended to use `conda` or `venv` to manage your environment.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Sam-Ayodeji/causal-crypto-sentiment-analysis.git
    cd Crypto-Sentiment-Causal-ML
    ```

2.  **Install dependencies:**
    All required packages are automatically installed by the first cell in the Jupyter notebook. Alternatively, you can install them manually:
    ```bash
    pip install openpyxl doubleml scikit-learn statsmodels linearmodels scipy matplotlib seaborn requests
    ```

## Running the Notebook

Open and run the `Causal_ML_for_Sentiment_&_Crypto_(BTC_&_ETH)_Return_and_Volatility.ipynb` notebook in a Jupyter environment (e.g., Jupyter Lab, VS Code with Jupyter extension, or Google Colab).

-   **Google Colab**: The notebook is designed to run seamlessly in Google Colab. Simply upload it to Colab and run all cells.
-   **Local Jupyter**: Ensure all dependencies are installed and then open the notebook.

Run all cells sequentially to reproduce the analysis. The notebook is structured with clear headings and explanations for each section.

## Key Findings

*(contrarian effects, regime-dependent causal effects, etc.)*

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
