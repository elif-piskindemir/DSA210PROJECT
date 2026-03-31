
## Title
Anomaly Detection in Water Distribution Networks Using Data-Driven Methods

## Proposal

In this project, I aim to analyze water distribution network data to detect abnormal conditions such as leaks, pressure drops, or irregular flow patterns. Efficient water management is a critical real world problem and early detection of anomalies can help prevent water loss, reduce operational costs and improve infrastructure reliability. I chose this topic because water management is an important real world problem.

The main dataset for this project will come from publicly available water distribution datasets such as the DiTEC dataset. This dataset includes time-based measurements like pressure, flow rate, and demand values collected from different nodes and pipes in the system. It contains a large number of observations over time, which makes it suitable for analysis. Moreover, working with time-series data allows me to observe how the system behaves under different conditions and detect unusual patterns.

To satisfy the data enrichment requirement, I will either combine this dataset with another source or generate additional data. For example, I may use leak scenario datasets such as LeakDB or simulate anomalies by introducing realistic changes like sudden drops in pressure or irregular flow patterns. This will help me create labeled data that separates normal and abnormal situations. To delve deeper into the data, I will also create new features such as rolling averages, time-based indicators and change rates, which can make patterns more visible.

The data will be processed using Python, mainly with libraries such as pandas and NumPy. After cleaning the data and handling missing values, I will perform exploratory data analysis using matplotlib and seaborn to understand distributions and relationships. However, simply visualizing the data is not enough, so I will also apply hypothesis testing. For instance, I can test whether pressure values significantly change during abnormal conditions or whether certain flow patterns are related to leaks. Depending on the situation, I will use tests like t-tests or other appropriate methods.

Finally, in the machine learning stage, I will apply models such as Logistic Regression and Random Forest, as well as anomaly detection methods like Isolation Forest. The goal is to build a model that can identify whether the system is operating normally or not. This project follows the main steps of the data science pipeline and connects course concepts to a real-world problem. However, one limitation is that public datasets may not fully represent real-life systems, and synthetic anomalies may not perfectly match real leaks. As future work, more advanced models or real sensor data could be used to improve the results. All sources will be properly cited and any use of AI tools will be clearly stated.
