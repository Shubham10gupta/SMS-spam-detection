# SMS-spam-detection
SMS Spam classification is crucial for filtering unsolicited emails. Using the UCI SPAM SMS Database with 4601 instances and 57 features, we build a machine learning model to distinguish spam from non-spam. Key steps include data preprocessing, exploratory analysis, model training and evaluation, achieving robust SMS filtering.

SMS Spam Classification
Overview
SMS Spam classification is a critical task in natural language processing and cybersecurity, aiming to distinguish between legitimate emails and spam. Spam SMS include unwanted advertisements, phishing attempts, and other unsolicited messages. The goal of this project is to build a machine learning model that can accurately classify emails as spam or not spam using the SPAM E-mail Database from the UCI Machine Learning Repository.

Dataset
The dataset used in this project is the SPAM SMS Database from the UCI Machine Learning Repository. It contains 4601 instances with 57 continuous features and 1 nominal class label indicating whether an email is spam (1) or not spam (0). The features include the frequency of specific words and characters in the email and various metrics related to sequences of capital letters.

Data Characteristics
Number of Instances: 4601
Number of Attributes: 58 (57 continuous, 1 nominal class label)
Class Distribution: 39.4% spam, 60.6% non-spam
Attributes:
word_freq_WORD: Percentage of words in the email that match a specific word (e.g., 'word_freq_make').
char_freq_CHAR: Percentage of characters in the email that match a specific character (e.g., 'char_freq_!').
capital_run_length_average: Average length of uninterrupted sequences of capital letters.
capital_run_length_longest: Length of the longest uninterrupted sequence of capital letters.
capital_run_length_total: Total number of capital letters in the email.
Methodology
The project involves the following steps:

Data Loading and Preprocessing
Loaded the SMS Spam Collection Dataset and assigned appropriate column names (label, message).

Encoded the labels (ham as 0 and spam as 1).

Separated the dataset into features (SMS text) and labels (spam/ham).

Performed train-test split to divide the data for model training and evaluation.

Applied text preprocessing techniques:

Lowercasing, removing punctuation, stopwords, and lemmatization.

Converted text data into numerical format using TF-IDF Vectorization for efficient feature extraction.

Exploratory Data Analysis (EDA)
Examined class distribution to check for any imbalance between spam and ham messages.

Created word clouds and frequency plots to visualize commonly used terms in both classes.

Explored feature correlations and message lengths to uncover patterns between spam and ham texts.

Feature Selection
Initially used all features from the TF-IDF representation.

Explored feature importance and dimensionality reduction techniques to further optimize model performance.

Model Training and Evaluation
Trained multiple classification models:

Logistic Regression

Decision Tree

Random Forest

Support Vector Machine (SVM)

Multinomial Naive Bayes

Evaluated models using:

Accuracy

Classification report (Precision, Recall, F1-score)

Confusion matrix

Multinomial Naive Bayes outperformed other models, achieving the highest accuracy and precision, making it especially effective for text-based spam classification tasks.

Hyperparameter Tuning
Applied GridSearchCV to Logistic Regression and SVM to improve their performance.

Despite tuning, Multinomial Naive Bayes remained the best-performing model in terms of accuracy and generalization.

Model Testing
Tested the final Naive Bayes model on unseen SMS data to validate its effectiveness.

Maintained high performance, showing good generalization and minimal false positives.

Results
The Multinomial Naive Bayes model demonstrated the highest accuracy in classifying spam vs. ham messages. Its efficiency and performance in handling text data make it a robust and scalable choice for real-world SMS spam detection systems.

Conclusion
The SMS Spam Detection project successfully leveraged machine learning and natural language processing techniques to build an accurate and efficient spam classifier. By using TF-IDF for feature extraction and training various models, Multinomial Naive Bayes stood out as the most effective. This model can be integrated into messaging apps or email services to automatically detect and filter out spam messages, enhancing user experience and security.

