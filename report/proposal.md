
## Title
Anomaly Detection in Water Distribution Networks Using Data-Driven Methods

## Proposal

In this project, I aim to analyze water distribution network data to detect abnormal conditions such as leaks, pressure drops, or irregular flow patterns. Efficient water management is a critical real world problem and early detection of anomalies can help prevent water loss, reduce operational costs and improve infrastructure reliability. I chose this topic because water management is an important real world problem.

The main dataset for this project will come from publicly available water distribution datasets such as the DiTEC dataset. This dataset includes time-based measurements like pressure, flow rate, and demand values collected from different nodes and pipes in the system. It contains a large number of observations over time, which makes it suitable for analysis. Moreover, working with time-series data allows me to observe how the system behaves under different conditions and detect unusual patterns.

To satisfy the data enrichment requirement, I will either combine this dataset with another source or generate additional data. For example, I may use leak scenario datasets such as LeakDB or simulate anomalies by introducing realistic changes like sudden drops in pressure or irregular flow patterns. This will help me create labeled data that separates normal and abnormal situations. To delve deeper into the data, I will also create new features such as rolling averages, time-based indicators and change rates, which can make patterns more visible.

The data will be processed using Python, mainly with libraries such as pandas and NumPy. After cleaning the data and handling missing values, I will perform exploratory data analysis using matplotlib and seaborn to understand distributions and relationships. However, simply visualizing the data is not enough, so I will also apply hypothesis testing. For instance, I can test whether pressure values significantly change during abnormal conditions or whether certain flow patterns are related to leaks. Depending on the situation, I will use tests like t-tests or other appropriate methods.

Finally, in the machine learning stage, I will use models such as Logistic Regression and Random Forest and try anomaly detection methods like Isolation Forest. The main goal is to understand whether the system is in a normal or abnormal state based on the data. This project follows the basic steps of the data science process and helps me apply what I learned in class to a real problem. However, one limitation is that the dataset may not fully reflect real-life conditions and the simulated anomalies may not be exactly the same as real leaks. In the future, this work could be improved by using real sensor data or more advanced models.
