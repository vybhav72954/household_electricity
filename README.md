# Regression Analysis of U.S. Household Annual Electricity Consumption
### Using the 2020 EIA Residential Energy Consumption Survey

**Course:** Regression and Time Series Models (MA60056)  
**Instructor:** Dr. Buddhananda Banerjee  

### Team Members
- **Anmol Gulati** (25BM6JP04)
- **Pranav Taneja** (25BM6JP37)
- **Prateek Hegde** (25BM6JP39)
- **Sneha Yadav** (25BM6JP49)
- **Vybhav Chaturvedi** (25BM6JP60)

---

## Overview
This repository contains the primary sequence for an end-to-end regression analysis of annual household electricity consumption (KWH) using the 2020 Residential Energy Consumption Survey (RECS) microdata published by the U.S. Energy Information Administration (EIA).

The objective is to identify the dominant household-level drivers of electricity consumption using an interpretable OLS model with heteroskedasticity-robust standard errors and benchmarking against regularised and tree-based models. 

A full comprehensive report detailing our exploratory data analysis, methodology, and findings can be compiled from the `outputs/main.tex` source file.

## Repository Structure
- `recs_regression_workflow_v2.ipynb`: The main analytical notebook containing the end-to-end workflow, including data preprocessing, exploratory data analysis, multicollinearity diagnostics, feature selection, and model training.
- `outputs/`: Directory containing the LaTeX source (`main.tex`) and compiled report for the final analytical presentation.
- `requirements.txt`: Python package dependencies required to run the analytical workflow.

*(Note: Data pipelines and experimental notebooks are intentionally excluded from this standalone repository to focus strictly on the clean, reproducible pipeline).*

## Reproducibility Guide

The codebase was developed using Python and Jupyter Notebooks. To replicate the analysis, follow the practical instructions below:

### 1. Prerequisites
Ensure you have Python installed. We highly recommend using a virtual environment to isolate the project dependencies.

### 2. Setup Environment
Clone the repository and install the dependencies:
```bash
# Clone the repository
git clone https://github.com/vybhav72954/household_electricity.git
cd household_electricity

# Create a virtual environment (optional but recommended)
python -m venv .venv

# Activate the virtual environment
# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate

# Install the required packages
pip install -r requirements.txt
```

### 3. Fetching the Dataset
To keep the repository lightweight, the raw dataset is not included in the version control. 
1. Download the dataset from our **[Google Drive Folder](https://drive.google.com/drive/u/2/folders/1p8gR59MZd-9KokQtJyjXErHQvd-1BbWK)**.
2. Place the dataset file (`recs_dataset.csv`) directly in the root directory of the cloned repository.

*Alternatively, the original public data can be found directly from the [EIA 2020 RECS Website](https://www.eia.gov/consumption/residential/data/2020/).*

### 4. Executing the Analysis Pipeline
All code executes directly from the root working directory:

1. Launch Jupyter Notebook or Jupyter Lab:
   ```bash
   jupyter notebook
   ```
2. Open and run `recs_regression_workflow_v2.ipynb` sequentially from top to bottom. It will load the dataset, perform data extraction and feature engineering, and output all statistical models and regression diagnostics locally.
