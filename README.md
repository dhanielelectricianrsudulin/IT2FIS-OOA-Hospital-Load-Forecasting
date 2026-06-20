# IT2FIS-OOA Hospital Load Forecasting

This repository contains the complete datasets, preprocessing calculations, and MATLAB source codes for the research paper: 
**"A Hybrid Interval Type-2 Fuzzy Inference System-Orangutan Optimization Algorithm (IT2FIS-OOA) for Multi-Year Forecasting of Hospital Electrical Energy Consumption during Special Holidays"**.

This repository is strictly curated to ensure full transparency and reproducibility of the numerical results presented in the manuscript.

## 📁 Repository Contents

### 1. Dataset and Evaluation Metrics (Excel File)
* Contains the raw electrical load records from Ulin Regional Public Hospital spanning 2020 to 2024.
* Includes explicit chronological train-test splits (to prevent data leakage), preprocessing calculations (WDmax, LDmax, TLDmax, and VLDmax), and the fully compiled prediction results with evaluation metrics (R-squared, RMSE, MAE, and MAPE).

### 2. MATLAB Codes (Year 2023)
* A folder containing all forecasting scripts and rule-generation codes tested on the 2023 hold-out dataset.
* Includes independent implementations of the baseline and benchmark models: **Type-1 FIS**, **Standard IT2FIS**, **IT2FIS-CSA**, **IT2FIS-FA**, and the proposed **IT2FIS-OOA**.
* **Master Script (`Performanceresult2023.m`):** An automated script designed to execute 30 independent stochastic runs of the metaheuristic algorithms. Executing this script will automatically regenerate the statistical performance logs (Table 8), convergence curves (Fig. 7a), and statistical distribution boxplots (Fig. 8a) for the 2023 dataset.

### 3. MATLAB Codes (Year 2024)
* A folder containing all forecasting scripts and rule-generation codes tested on the 2024 hold-out dataset.
* Includes independent implementations of the baseline and benchmark models: **Type-1 FIS**, **Standard IT2FIS**, **IT2FIS-CSA**, **IT2FIS-FA**, and the proposed **IT2FIS-OOA**.
* **Master Script (`Performanceresult2024.m`):** An automated script designed to execute 30 independent stochastic runs of the metaheuristic algorithms. Executing this script will automatically regenerate the statistical performance logs (Table 8), convergence curves (Fig. 7b), and statistical distribution boxplots (Fig. 8b) for the 2024 dataset.

### 4. IT2FLT Folder Toolbox
* Contains the **Interval Type-2 Fuzzy Logic Toolbox** developed by Prof. Oscar Castillo. 
* This toolbox is included directly in this repository to ensure reviewers and readers have the exact dependency required to run the scripts smoothly without versioning conflicts.

## ⚙️ System Requirements
* **MATLAB R2013a** (or compatible versions).
* **Interval Type-2 Fuzzy Logic Toolbox** (already included in folder #4).

## 🚀 Reproducibility Guide
To independently run the source codes and verify the numerical results, please follow these steps:
1. Download or clone this entire repository to your local machine.
2. Open MATLAB and add the IT2FLT Toolbox folder to your MATLAB path. *(Right-click the toolbox folder in the Current Folder browser -> Select "Add to Path" -> "Selected Folders and Subfolders")*.
3. Ensure the Excel dataset file is placed in the same working directory as the MATLAB scripts you wish to execute.
4. To verify individual forecasting accuracy, execute specific algorithm scripts (e.g., `IT2FISOOA2023.m`). 
5. To automatically verify the overall statistical robustness and regenerate the charts presented in the manuscript's evaluation tables, simply run the **`Performanceresult2023.m`** or **`Performanceresult2024.m`** scripts.
