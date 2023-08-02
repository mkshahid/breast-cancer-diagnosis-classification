# breast-cancer-diagnosis-classification

# Description
This project focuses on leveraging machine learning techniques to classify and diagnose breast cancer from the Wisconsin Breast Cancer Dataset, and authenticate banknotes from the Banknote Authentication Dataset. The project explores Supervised, Semi-Supervised, and Unsupervised Learning, as well as Active Learning Using Support Vector Machines.

# Part 1: Breast Cancer Diagnosis Classification
The Breast Cancer Wisconsin (Diagnostic) Data Set is used. The data set comprises IDs, classes (Benign=B, Malignant=M), and 30 attributes, with two output classes.

# Procedures
1. Supervised Learning: An L1-penalized SVM is trained to classify the data, using 5 fold cross-validation to choose the penalty parameter. The data is normalized and the model's accuracy, precision, recall, F1-score, and AUC are reported for both training and test sets over M runs.
2. Semi-Supervised Learning/Self-training: 50% of the positive class and 50% of the negative class in the training set is selected as labeled data, and the rest as unlabeled data. An L1-penalized SVM is trained to classify the labeled data, and unlabeled data points are added and classified iteratively. The model's accuracy, precision, recall, F1-score, and AUC are reported for both training and test sets over M runs.
3. Unsupervised Learning: The k-means algorithm is run on the whole training set, with k=2. The algorithm is initialized randomly and run multiple times to avoid local minima. The centers of the two clusters are computed and the closest 30 data points to each center are used to predict labels via a majority poll. The labels provided by k-means are compared with the true labels and the model's accuracy, precision, recall, F1-score, and AUC are reported over M runs.
4. Spectral Clustering: The same procedures as in Unsupervised Learning are followed, but using spectral clustering instead of k-means.
5. Comparison of methods: The results obtained from supervised learning on the full data set, semi-supervised learning with half of the data set labeled, and unsupervised learning are compared.
