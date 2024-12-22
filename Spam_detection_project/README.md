Email Spam Detection Project

This project focuses on building a machine learning model to classify emails as either "Spam" or "Ham" (non-spam). The goal is to identify spam emails based on their content using natural language processing (NLP) techniques and classification algorithms.

Table of Contents

Introduction

Dataset

Project Workflow

Technologies Used

Evaluation Metrics

Results

Future Improvements

How to Run the Project



---

Introduction

Email spam detection is a common problem in natural language processing (NLP). Spam emails often contain specific patterns, keywords, and structures that distinguish them from legitimate emails. In this project, we preprocess the email data, extract meaningful features using TF-IDF, and use a Naive Bayes classifier to detect spam emails.


---

Dataset

The project uses a CSV file containing email content labeled as either spam (1) or ham (0).

Number of Emails: 5,572 (example size for explanation)

Features Used: Email text (as raw content) and corresponding labels.

The dataset was split into 70% training and 30% testing to train and evaluate the model.



---

Project Workflow

1. Data Preprocessing:

Remove missing values and clean email content.

Convert text to lowercase and remove punctuation, special characters, and hyperlinks.



2. Feature Extraction:

Use TF-IDF (Term Frequency-Inverse Document Frequency) vectorization to convert email text into numerical format suitable for machine learning.



3. Model Training:

Train a Naive Bayes classifier on the training set.



4. Model Evaluation:

Evaluate the model on the test set using precision, recall, F1-score, and accuracy metrics.

Analyze the confusion matrix to understand the model's strengths and weaknesses.



5. Key Features Analysis:

Extract and display the top words most indicative of spam emails (e.g., "free", "click", "money").



6. ROC Curve Visualization:

Plot and interpret the Receiver Operating Characteristic (ROC) curve to measure model performance.





---

Technologies Used

Programming Language: Python

Libraries:

pandas for data manipulation.

scikit-learn for machine learning and evaluation.

matplotlib for data visualization.

numpy for numerical operations.




---

Evaluation Metrics

The following metrics were used to evaluate the model's performance:

Precision: How many predicted spam emails were actually spam.

Recall: How many actual spam emails were correctly identified.

F1-Score: Harmonic mean of precision and recall, balancing both metrics.

Accuracy: Overall percentage of correct predictions.

Confusion Matrix: Breaks down predictions into true positives, false positives, true negatives, and false negatives.



---

Results

Accuracy: 89%

Precision (Spam): 100%

Recall (Spam): 40%

Top Spam-Indicating Features:

"number": -6.41

"hyperlink": -6.81

"click": -7.39

"free": -7.50

"money": -8.01



Confusion Matrix: |              | Predicted Ham | Predicted Spam | |--------------|---------------|----------------| | Actual Ham | 741           | 0              | | Actual Spam | 95            | 64             |


---

Future Improvements

To enhance the project further:

1. Dataset:

Use a larger, more diverse dataset to improve generalization.

Include more features, such as email metadata (e.g., sender domain, subject line).



2. Handle Class Imbalance:

Use techniques like oversampling (e.g., SMOTE) or undersampling to improve recall for spam emails.



3. Try Advanced Algorithms:

Experiment with models like Logistic Regression, Random Forest, or Gradient Boosting.



4. Use Word Embeddings:

Replace TF-IDF with advanced text representations like Word2Vec, GloVe, or BERT.



5. Deploy the Model:

Build a Flask or FastAPI web application for real-time spam predictions.


