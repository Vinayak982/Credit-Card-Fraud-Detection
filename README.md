Credit Card Fraud Detection



This project focuses on detecting fraudulent credit card transactions using machine learning techniques. The dataset used is highly imbalanced, with a significantly higher number of non-fraudulent transactions compared to fraudulent ones. To address this imbalance, techniques like SMOTE (Synthetic Minority Over-sampling Technique) have been employed to improve the model's performance.

Table of Contents
Project Overview
Dataset
Techniques Used
Modeling
Evaluation
Conclusion
Future Work
Installation
Usage
Contributing
License
Project Overview
The goal of this project is to build a model that can accurately detect fraudulent transactions from credit card data. The challenges include dealing with the severe class imbalance and ensuring the model's performance is robust enough for real-world application.

Dataset
The dataset consists of credit card transactions, labeled as fraudulent or non-fraudulent. Given the sensitive nature of the data, it has been anonymized.

Features: 30 features, including the transaction amount and anonymized variables V1, V2, ..., V28.
Target: Binary classification - 1 for fraud and 0 for non-fraud.
Techniques Used
Data Preprocessing: Handling missing values, scaling features, and dealing with class imbalance.
Outlier Detection: Identifying and removing outliers, particularly in the undersampled dataset.
Resampling Techniques: Using SMOTE to balance the dataset by generating synthetic samples for the minority class (fraudulent transactions).
Neural Networks: Building and training neural networks to predict fraudulent transactions.
Modeling
Various machine learning models were tested, with a focus on neural networks. The models were trained on both undersampled and oversampled datasets.

Evaluation
The models were evaluated using standard classification metrics such as accuracy, precision, recall, F1-score, and AUC-ROC. Special attention was given to the trade-off between detecting fraud and minimizing false positives (i.e., incorrectly classifying non-fraudulent transactions as fraudulent).

Conclusion
Implementing SMOTE on our imbalanced dataset helped mitigate the issue of label imbalance (more non-fraudulent than fraudulent transactions). However, it's important to note that the neural network on the oversampled dataset sometimes predicts fewer correct fraud transactions compared to the model using the undersampled dataset.

Key observations:

The undersampled model, while better at detecting fraud, tends to misclassify a significant number of non-fraudulent transactions as fraud. This could lead to customer dissatisfaction and an increase in complaints if legitimate transactions are wrongly flagged.
Outlier removal was applied only to the undersampled dataset. This might have influenced the model's performance on this data compared to the oversampled dataset.
The next step is to apply outlier removal to the oversampled dataset and evaluate if this improves the model's accuracy on the test set.
Future Work
Apply outlier detection and removal to the oversampled dataset.
Explore additional resampling techniques and models.
Fine-tune the neural network architecture for better performance.
Implement a cost-sensitive learning approach to penalize misclassifications more appropriately.
Installation
To run this project, you will need to install the following dependencies:

bash
Copy code
pip install -r requirements.txt
Usage
You can start by exploring the data, preprocessing, and then running the models using the provided Jupyter notebooks. The main script to train and evaluate the models is credit_card_fraud_detection.ipynb.

Contributing
Contributions are welcome! If you have any suggestions, feel free to create an issue or submit a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

This README provides an overview of the project, including the challenges, techniques used, and next steps.
