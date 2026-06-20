# IT2FIS-OOA Hospital Load Forecasting

This repository contains the complete datasets, preprocessing calculations, and MATLAB source codes for the research paper: 
**"A Hybrid Interval Type-2 Fuzzy Inference System-Orangutan Optimization Algorithm (IT2FIS-OOA) for Multi-Year Forecasting of Hospital Electrical Energy Consumption during Special Holidays"**.

This repository is strictly curated to ensure full transparency and reproducibility of the numerical results presented in the manuscript.

## 📁 Repository Contents

### 1. Dataset and Evaluation Metrics (Excel)
* **Raw Data & Preprocessing:** Contains the raw electrical load records from Ulin Regional Public Hospital spanning 2020 to 2024.
* **Chronological Train-Test Split:** Explicitly defines the data partitioning to prevent data leakage (2020-2022 for FoU optimization training, 2023-2024 for independent hold-out testing).
* **Calculated Indicators:** Step-by-step spreadsheet calculations for WDmax, LDmax, TLDmax, and VLDmax.
* **Final Results:** The fully compiled prediction results and evaluation metrics (R-squared, RMSE, MAE, and MAPE) corresponding to the tables in the manuscript.

### 2. Primary Forecasting Models (MATLAB Scripts)
* **Type-1 FIS:** Baseline fuzzy logic forecasting implementation.
* **Standard IT2FIS:** Interval Type-2 fuzzy logic forecasting implementation.
* **IT2FIS-OOA (2023 & 2024):** The proposed hybrid algorithm scripts. These scripts integrate the IT2FIS fuzzy rule-generation codes with the Orangutan Optimization Algorithm (OOA). They contain fixed algorithm hyperparameters, search space boundaries, and optimization logs for regenerating the final forecast results.

### 3. Benchmark Models and Statistical Validation (MATLAB Scripts)
* **Benchmark Algorithms:** Source codes for the comparative models, including Cuckoo Search Algorithm (CSA), Firefly Algorithm (FA), and Zebra Optimization Algorithm (ZOA).
* **Generate_Table_8.m:** A specific script designed to independently verify the statistical robustness of the proposed method. Running this script will execute 30 independent stochastic runs for the OOA, CSA, FA, and ZOA algorithms, automatically outputting the 'Best' (minimum objective error) and 'Standard Deviation' logs to regenerate Table 8.

## ⚙️ System Requirements
To independently run the source codes and verify the results, the following environment is required:
* **MATLAB R2013a** (or compatible versions).
* **Interval Type-2 Fuzzy Logic Toolbox** developed by Prof. Oscar Castillo.

## 🚀 Reproducibility Guide
1. Ensure the dataset (`.xls` or `.xlsx`) is located in the same working directory as the MATLAB scripts.
2. To verify the multi-year forecasting accuracy, execute the `IT2FIS_OOA_2023.m` and `IT2FIS_OOA_2024.m` scripts.
