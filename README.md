This project demonstrates how to apply logistic regression to a binary classification problem, using a classic cancer detection dataset. The notebook leads you through data preparation, model training, evaluation, threshold tuning, and interpretation.

Steps Illustrated
1. Data Selection and Loading
Chosen dataset: Breast cancer diagnosis data (commonly used for binary classification tasks).

Loaded using pandas, with "diagnosis" as the target (Malignant = 1, Benign = 0).

2. Train/Test Splitting and Standardization
Data split into training (80%) and test (20%) sets using train_test_split, preserving class balance.

Features standardized using StandardScaler to give each feature a mean of 0 and variance of 1.

Standardization helps logistic regression converge efficiently and perform well, especially when features vary in scale.

3. Model Fitting
Logistic Regression (from sklearn) is trained on the standardized features.

Logistic regression predicts the probability that each sample belongs to class 1 using the sigmoid function.


4. Evaluation
Performance is checked with:

Confusion matrix (shows counts of true/false positives/negatives)

Precision (correctness of positive predictions)

Recall (ability to find all positive cases)

ROC-AUC (how well predictions separate classes)

The default prediction threshold is 0.5.

5. Threshold Tuning & Sigmoid Explanation
Thresholds below 0.5 make the classifier more "sensitive" (higher recall at the cost of lower precision), suitable for applications where missing positives is costly.

Sigmoid function maps continuous model outputs to probabilities between 0 and 1.

Adjusting the "decision threshold" affects the trade-off between precision and recall — you can tune this depending on your needs.
