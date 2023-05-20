# anomaly-detection-algorithm-to-detect-anomalous-behavior-in-computer-servers

This repository contains MATLAB code for performing anomaly detection using multivariate probability distributions. The code is based on a dataset consisting of two variables: "Throughput" and "Latency". Anomalies in the dataset are identified by comparing the probability of each data point with a predefined threshold.



### What was my motivation?

My motivation for this project was to develop an anomaly detection algorithm using multivariate probability distributions. Anomaly detection is a valuable technique in various domains, including fraud detection, network security, and system monitoring. I wanted to explore and understand the concepts and techniques involved in identifying anomalies in datasets.

### Why did I build this project?

I built this project to gain hands-on experience in anomaly detection and understand how multivariate probability distributions can be used for this purpose. By building this project, I aimed to enhance my understanding of probability modeling, statistical analysis, and data visualization techniques in MATLAB.

### What problem does it solve?

The project addresses the problem of detecting anomalies in datasets based on multivariate probability distributions. Anomalies are data points that deviate significantly from the normal behavior of the dataset. By fitting a probability distribution to the data, we can quantify the likelihood of each data point and set a threshold to classify anomalies. The project provides a framework to visualize the data, fit distributions, compute probabilities, and evaluate the performance of the anomaly detection model.

### What did I learn?

Through this project, I learned:

The concept of anomaly detection and its importance in various applications.
The use of multivariate probability distributions, such as the normal and t-distributions, for modeling complex data.
Techniques for visualizing data distributions, including scatter plots, histograms, and probability contour plots.
The evaluation metrics for assessing the performance of anomaly detection models, such as precision, recall, and F1 score.
How to use MATLAB functions and libraries for data analysis, probability modeling, and visualization.
The process of interpreting ROC curves and comparing the performance of different models based on AUC values.

## Installation
To use this code, make sure you have MATLAB installed on your system. Simply clone this repository or download the code files to your local machine.

## Usage
Load the dataset: The code starts by loading a dataset (data1.mat) which contains the "Throughput" and "Latency" variables. The dataset is organized into a table (dataval) with columns representing the variables and a binary indicator for anomalies.

## Data Visualization:

Scatterhist Plot: The code generates a scatterhist plot to visualize the relationship between "Throughput" and "Latency" variables. Anomalies are marked with 'x' markers.
Histogram and Distribution Fits: The code creates a figure with four subplots showing histogram and distribution fits for both variables. Two types of fits are shown: normal distribution and t-distribution fits.
Probability Contour Plot: The code generates a probability contour plot based on the multivariate probability distribution fitted to the data. An epsilon value is set as a threshold to classify anomalies. Anomalies are marked in red, and misclassified points are shown as magenta circles.

## Evaluation:

Confusion Matrix: The code computes a confusion matrix to evaluate the performance of the anomaly detection model. Precision, recall, and F1 score are calculated based on the confusion matrix.
Receiver Operating Characteristic (ROC) Curve: The code generates an ROC curve to visualize the trade-off between true positive rate (sensitivity) and false positive rate (1-specificity). The optimal threshold is determined by selecting the point on the curve closest to the top-left corner.
Full Covariance Model: An alternative probability model with a full covariance matrix is computed. The ROC curve and area under the curve (AUC) are calculated and compared with the independent variable model.

## Results

The code displays various plots and outputs to provide insights into the anomaly detection process. The key results include:

Scatterhist plot to visualize the data distribution and identify anomalies.
Histogram and distribution fits for both variables.
Probability contour plot showing the decision boundary and misclassified points.
Confusion matrix, precision, recall, and F1 score to evaluate the model performance.
ROC curve for the independent variable model and the full covariance model.
Comparison of AUC values between the independent and full covariance models.

## License

This code is released under the MIT License. Feel free to use, modify, and distribute the code for both commercial and non-commercial purposes. Please refer to the LICENSE file for more details.

## Acknowledgements

The code is developed as part of an anomaly detection project and utilizes various MATLAB functions and libraries. It is provided as a reference implementation and can be further customized or extended based on specific requirements.
