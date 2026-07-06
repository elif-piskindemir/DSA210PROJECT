# Anomaly Detection in Water Distribution Networks Using Data-Driven Methods

## Motivation

Water distribution systems are critical infrastructures that provide clean water to cities and communities. Detecting anomalies such as leaks, abnormal pressure drops, or irregular flow patterns is important for reducing water loss and improving system reliability. In this project, I aimed to analyze water distribution network data using data science techniques and machine learning methods to identify abnormal system behavior. I chose this topic because it combines real world engineering problems with data analysis and machine learning applications.

---

## Data Source

The main dataset used in this project was obtained from the DiTEC Water Distribution Network Dataset:

- https://github.com/DiTEC-project/DiTEC_WDN_dataset

The dataset contains sensor-based information such as pressure, flow, and demand values collected from water distribution systems. Publicly available datasets were enriched through preprocessing and additional analysis steps.

The project mainly focused on numerical sensor measurements and anomaly-related patterns in the system.

---

## Data Preparation

The dataset was processed using Python libraries such as:

- pandas
- numpy
- matplotlib
- scikit-learn

The preprocessing stage included:

- Handling missing values
- Removing unnecessary columns
- Normalizing numerical values
- Organizing the data into analyzable formats
- Feature selection for machine learning models

The cleaned dataset was then used for exploratory data analysis and machine learning tasks.

---

## Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to better understand the structure of the dataset and detect patterns.

The following analyses were conducted:

- Distribution analysis of sensor values
- Correlation analysis between variables
- Visualization of pressure and flow patterns
- Detection of outliers and abnormal values

Different plots and visualizations were generated using matplotlib to observe system behavior and identify potential anomalies.

---

## Hypothesis Testing

Basic statistical analysis and hypothesis testing techniques were applied during the project.

The goal was to investigate whether abnormal sensor behavior significantly differed from normal operating conditions.

The analysis helped evaluate whether certain sensor measurements showed statistically meaningful deviations under anomaly conditions.

---

## Machine Learning Methods

Several machine learning methods were applied to the dataset to detect anomalies and classify system behavior.

The implemented methods included:

### Logistic Regression

Logistic Regression was used as a baseline classification model to distinguish between normal and abnormal conditions.

### Random Forest

Random Forest was applied to improve classification performance and analyze feature importance.

### Isolation Forest

Isolation Forest was used as an anomaly detection algorithm because it is effective for identifying unusual observations in large datasets.

The models were trained and evaluated using the prepared dataset.

---

## Findings

The analysis showed that machine learning methods can successfully detect abnormal patterns in water distribution network data.

Among the tested models, Random Forest and Isolation Forest produced stronger results for identifying anomalies compared to simpler baseline methods.

The project also demonstrated that preprocessing and feature selection significantly affect model performance.

Visual analysis revealed noticeable differences between normal and abnormal sensor behavior.

The machine learning results showed that Logistic Regression achieved an accuracy of approximately 90.10% (due to predicting the majority class of normal system status), Random Forest achieved a realistic accuracy of 92.57%, and Isolation Forest achieved approximately 81.19% accuracy on the test set. 

Initially, the Random Forest model achieved a suspicious 100% accuracy due to two main bugs:
1. **Target Leakage:** The anomaly labels were defined based on the lowest 10% of `min_pressure`. However, the training features included `max_pressure` and `pressure_range` (which is calculated as `max_pressure - min_pressure`), allowing the tree-based models to mathematically reconstruct `min_pressure` perfectly and memorize the classification threshold.
2. **Feature Corruption:** The `time` column was accidentally included in calculating the row-wise summary statistics (like `mean_pressure` and `max_pressure`) in the final machine learning pipeline, which skewed the features since time increases linearly.

To fix these issues, we corrected the `time` column bug and removed the leaking features (`min_pressure` and `pressure_range`) from the input variables of the contemporaneous models. As a result, the Random Forest classifier achieved a scientifically sound and generalizable test accuracy of 92.57% (correctly identifying 5 out of 20 anomalies with zero false positives).

---

## Limitations and Future Work

One limitation of this project is that publicly available datasets may not perfectly represent real world water distribution systems. Some anomalies may also be synthetic rather than naturally occurring.

Future improvements could include:

- Using larger and more realistic datasets
- Applying deep learning methods
- Integrating real-time sensor streams
- Comparing additional anomaly detection algorithms
- Building a real-time monitoring dashboard
---

## AI Assistance Disclosure

AI tools were used during this project for debugging support, explanation of programming concepts and improvement of documentation.

All implementation decisions, data analysis steps, and project organization were reviewed and completed by me, Elif Pişkindemir.

---

## References

1. DiTEC Water Distribution Network Dataset  
   https://github.com/DiTEC-project/DiTEC_WDN_dataset

2. Python Documentation  
   https://www.python.org/

3. Scikit-learn Documentation  
   https://scikit-learn.org/

