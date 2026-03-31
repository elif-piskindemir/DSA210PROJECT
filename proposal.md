## Title
Anomaly Detection in Water Distribution Networks Using Data-Driven Methods

## Proposal

In this project, I aim to analyze water distribution network data to detect abnormal conditions such as leaks or pressure failures. This topic is important because efficient water management is a critical real-world problem, and early detection of anomalies can prevent resource loss and infrastructure damage.

The main dataset will be obtained from the DiTEC water distribution dataset, which contains time-series data such as pressure, flow, and demand values across different nodes and pipes in a network. To enrich the dataset, I plan to incorporate additional leakage scenario data from sources such as LeakDB or generate synthetic anomalies based on realistic assumptions (e.g., sudden drops in pressure or irregular flow patterns).

The dataset is expected to contain time-series records across multiple nodes, providing sufficient observations for statistical analysis and machine learning. In the data analysis phase, I will perform preprocessing, feature engineering (such as rolling averages and change detection), and exploratory data analysis to understand patterns in the system. I will also apply hypothesis testing to investigate whether anomalies significantly affect pressure and flow variables.

In the machine learning stage, I will implement classification and anomaly detection methods such as Logistic Regression, Random Forest, and Isolation Forest to identify abnormal system behavior. The goal is to build a model that can distinguish between normal and anomalous operating conditions.
