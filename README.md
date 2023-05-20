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

# additional

# Multivariate probability model to the high dimensional dataset


This project implements an anomaly detection algorithm using multivariate probability distributions in MATLAB. The algorithm fits a multivariate normal distribution to the input dataset and uses it to quantify the likelihood of each data point. By setting an appropriate threshold, anomalies can be identified based on their low probability values.


### What was my motivation?

Our motivation behind this project was to develop an effective anomaly detection algorithm using multivariate probability distributions. We aimed to explore how such a technique could be utilized to identify outliers in datasets and provide valuable insights for various applications.

### Why did I build this project?

We built this project to address the need for robust anomaly detection methods that can handle multivariate data. Anomalies or outliers often represent significant deviations from normal behavior and can be indicators of potential issues or interesting patterns in a dataset. By developing this project, we aimed to provide a reliable tool for detecting anomalies and supporting decision-making processes in various domains.

### What problem does it solve?

This project solves the problem of identifying anomalies or outliers in multivariate datasets. By fitting a multivariate normal distribution to the data and setting an appropriate threshold, the algorithm is able to classify data points as normal or anomalous based on their probability values. This approach can be applied to various domains such as fraud detection, network intrusion detection, quality control, and outlier analysis in financial or healthcare datasets.

### What did I learn?

Through the development of this project, we gained a deeper understanding of multivariate probability distributions and their application in anomaly detection. We learned how to compute the mean and covariance matrix of multivariate data, calculate multivariate probability densities, evaluate performance using ROC curves, and determine optimal thresholds for anomaly detection. Additionally, we enhanced our skills in data visualization and interpretation of confusion matrices. This project provided practical insights into implementing an anomaly detection algorithm and reinforced our knowledge of probability theory and statistical analysis.


## Prerequisites

MATLAB (R2018a or later)

## Installation

To use this code, make sure you have MATLAB installed on your system. Simply clone this repository or download the code files to your local machine.


## Workflow

The dataset is loaded from data2.mat, which contains the input features (Xval) and corresponding labels (yval).
The mean (mu) and covariance matrix (sigma2) of the input features are computed using the mean() and cov() functions, respectively.
The multivariate probability densities of the input data points are calculated using the mvnpdf() function with the mean and covariance matrix.
The Receiver Operating Characteristic (ROC) curve is generated using the perfcurve() function, which plots the true positive rate against the false positive rate for different threshold values.
The optimal threshold (Topt) is determined based on the maximum value of the Youden's J statistic, obtained from the ROC curve.
The confusion matrix is computed using the confusionmat() function, which compares the predicted outliers (based on the threshold) with the true labels.
The ROC curve and the optimal threshold point are plotted using the plot() function.
The number of outliers predicted by the model is calculated by evaluating the multivariate probability densities of the entire dataset (X) and counting the number of points below the threshold (Topt).

## Results

The optimal threshold (Topt) is printed to the console, indicating the value that maximizes the performance of the model.
The confusion matrix is displayed, showing the number of true positives, true negatives, false positives, and false negatives.
The ROC curve is plotted, visualizing the trade-off between the true positive rate and the false positive rate.
The number of outliers predicted by the model is printed to the console.

## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgements

The code is developed as part of an anomaly detection project and utilizes various MATLAB functions and libraries. It is provided as a reference implementation and can be further customized or extended based on specific requirements.

