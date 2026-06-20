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

### 3. MATLAB Codes (Year 2024)
* A folder containing all forecasting scripts and rule-generation codes tested on the 2024 hold-out dataset.
* Includes independent implementations of the baseline and benchmark models: **Type-1 FIS**, **Standard IT2FIS**, **IT2FIS-CSA**, **IT2FIS-FA**, and the proposed **IT2FIS-OOA**.

### 4. IT2FLS Toolbox
* Contains the **Interval Type-2 Fuzzy Logic Toolbox** developed by Prof. Oscar Castillo. 
* This toolbox is included directly in this repository to ensure reviewers and readers have the exact dependency required to run the scripts smoothly without versioning conflicts.

## ⚙️ System Requirements
* **MATLAB R2013a** (or compatible versions).
* **Interval Type-2 Fuzzy Logic Toolbox** (already included in folder #4).

## 🚀 Reproducibility Guide
To independently run the source codes and verify the numerical results, please follow these steps:
1. Download or clone this entire repository to your local machine.
2. Open MATLAB and add the IT2FLS Toolbox folder to your MATLAB path. *(Right-click the toolbox folder in the Current Folder browser -> Select "Add to Path" -> "Selected Folders and Subfolders")*.
3. Ensure the Excel dataset file is placed in the same working directory as the MATLAB scripts you wish to execute.
4. Open any algorithm script from the 2023 or 2024 folders (e.g., executing `IT2FIS00A2023.m`) and run it to verify the forecasting accuracy and statistical robustness presented in the paper's evaluation tables.
