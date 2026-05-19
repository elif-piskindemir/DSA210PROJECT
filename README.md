# Anomaly Detection in Water Distribution Networks Using Data-Driven Methods

## Project Overview

This project analyzes water distribution network data to detect abnormal system behavior such as low-pressure patterns, irregular sensor readings, and possible anomaly conditions.

The goal of the project is to apply the main steps of the data science pipeline, including data collection, preprocessing, exploratory data analysis, hypothesis testing, and machine learning.

## Motivation

Water distribution networks are critical infrastructures. Detecting abnormal behavior in these systems can help reduce water loss, identify possible leaks, and improve the reliability of water management systems.

I chose this topic because it connects a real-world engineering problem with data analysis and machine learning techniques.

## Data Source

The project uses publicly available water distribution network data from the DiTEC Water Distribution Network Dataset.

Dataset source:

https://github.com/DiTEC-project/DiTEC_WDN_dataset

The repository includes raw network input files and processed pressure data used for analysis.

## Repository Structure

DSA210PROJECT/
- data/
  - raw/
  - processed/
- report/
  - proposal.md
  - proposal.pdf
  - final_report.md
- ditec_processing.ipynb
- eda.ipynb
- requirements.txt
- README.md

## Methodology

The project follows these main steps:

1. Collect water distribution network data
2. Process raw network files
3. Generate and clean pressure-related data
4. Perform exploratory data analysis
5. Visualize sensor behavior and pressure patterns
6. Apply hypothesis testing
7. Create anomaly labels based on low-pressure behavior
8. Apply machine learning methods for anomaly detection
9. Evaluate and compare model results

## Machine Learning Methods

The final machine learning stage includes:

- Logistic Regression
- Random Forest
- Isolation Forest

Logistic Regression is used as a baseline supervised model. Random Forest is used as a stronger supervised classification model. Isolation Forest is used as an unsupervised anomaly detection method.

Since the dataset does not contain manually verified anomaly labels, anomaly labels are created using a statistical threshold based on unusually low minimum pressure values.

## How to Run

First, install the required dependencies:

```bash
pip3 install -r requirements.txt
```

Then open Jupyter Notebook:

```bash
jupyter notebook
```

Open and run the following notebooks:

- ditec_processing.ipynb
- eda.ipynb

## Requirements

The main Python libraries used in this project are:

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn
- wntr
- jupyter

## Final Report

The final report is available in the report folder:

report/final_report.md

The report includes the motivation, data source, data preparation, exploratory data analysis, hypothesis testing, machine learning methods, findings, limitations, future work, and AI assistance disclosure.

## AI Assistance Disclosure

AI tools were used for debugging support, explanation of programming concepts, and improvement of documentation and report writing. All implementation decisions, analysis steps, and final project organization were reviewed and completed by the student.

## References

- DiTEC Water Distribution Network Dataset: https://github.com/DiTEC-project/DiTEC_WDN_dataset
- Python Documentation: https://www.python.org/
- Scikit-learn Documentation: https://scikit-learn.org/
- WNTR Documentation: https://wntr.readthedocs.io/
