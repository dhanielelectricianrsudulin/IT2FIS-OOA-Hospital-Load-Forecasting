# IT2FIS-OOA Hospital Load Forecasting

This repository contains the complete datasets, preprocessing calculations, and MATLAB source codes for the research paper: 
**"A Hybrid Interval Type-2 Fuzzy Inference System-Orangutan Optimization Algorithm (IT2FIS-OOA) for Multi-Year Forecasting of Hospital Electrical Energy Consumption during Special Holidays"**.

This repository is strictly curated to ensure full transparency and reproducibility of the numerical results presented in the manuscript.

## 📁 Repository Contents

### 1. Dataset and Evaluation Metrics (`forecasting RSUD ULIN revisi 5 new.xlsx`)
* Contains the raw electrical load records from Ulin Regional Public Hospital spanning 2020 to 2024.
* Includes explicit chronological train-test splits (to prevent data leakage), preprocessing calculations (WDmax, LDmax, TLDmax, and VLDmax), Rule base, and the fully compiled prediction results with evaluation metrics (R-squared, RMSE, MAE, and MAPE).

### 2. MATLAB Codes & Results (Year 2023)
A dedicated directory containing the evaluation materials for the 2023 testing scenario. 
* **Dataset (`datafix2023.xls`):** The hold-out evaluation dataset containing the historical parameters and target VLDmax for the 14 special holidays in 2023.
* **Forecasting Scripts (`.m` files):** Standalone implementations of the baseline and benchmark models, including `T1FIS.m`, `IT2FIS.m`, `IT2FISCSA2023.m`, `IT2FISFA2023.m`, `IT2FISZOA2023.m`, and the proposed `IT2FISOOA2023.m`.
* **Master Script (`Performanceresult2023.m`):** An automated script designed to execute 30 independent stochastic runs of the metaheuristic algorithms.
* **Optimization Logs (`Optimization_Logs_2023_2.csv`):** The raw statistical performance log containing the absolute fitness values (MAE) from the 30 independent runs.
* **Visual Evidence (`FitnessCurve2023.jpg` & `Boxplot2023.jpg`):** High-resolution charts generated directly from the optimization logs, visually confirming the superior convergence speed and statistical robustness of the proposed IT2FIS-OOA model against the benchmarks.

### 3. MATLAB Codes & Results (Year 2024)
A dedicated directory containing the evaluation materials for the 2024 testing scenario.
* **Dataset (`datafix2024.xls`):** The hold-out evaluation dataset for the 14 special holidays in 2024.
* **Forecasting Scripts (`.m` files):** Standalone implementations of the baseline and benchmark models for the 2024 data parameters.
* **Master Script (`Performanceresult2024.m`):** An automated script designed to execute 30 independent stochastic runs of the metaheuristic algorithms. 
* **Optimization Logs & Visualizations:** Contains the raw statistical performance log (`Optimization_Logs_2024.csv`), alongside the generated **Convergence Curve** and **Statistical Distribution Box Plot** for the year 2024.

### 4. IT2FLT Folder Toolbox
* Contains the **Interval Type-2 Fuzzy Logic Toolbox** developed by Prof. Oscar Castillo. 
* This toolbox is included directly in this repository to ensure reviewers and readers have the exact dependency required to run the scripts smoothly without versioning conflicts.

## ⚙️ System Requirements
* **MATLAB R2013a** (or compatible modern versions).
* **Interval Type-2 Fuzzy Logic Toolbox** (already included in folder #4).

## 🚀 Reproducibility Guide
To independently run the source codes and verify the numerical results, please follow these steps:
1. Download or clone this entire repository to your local machine.
2. Open MATLAB and add the IT2FLT Toolbox folder to your MATLAB path. *(Right-click the toolbox folder in the Current Folder browser -> Select "Add to Path" -> "Selected Folders and Subfolders")*.
3. Ensure the Excel dataset file (e.g., `datafix2023.xls`) is placed in the same working directory as the MATLAB scripts you wish to execute.
4. To verify individual forecasting accuracy, execute specific algorithm scripts (e.g., `IT2FISOOA2023.m`). 
5. To automatically verify the overall statistical robustness and regenerate the charts presented in the manuscript's evaluation tables, simply run the **`Performanceresult2023.m`** or **`Performanceresult2024.m`** scripts.
