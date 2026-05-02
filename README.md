# machine_learning_final
# Predicting Student Academic Performance Using Machine Learning

## Project Overview

This project uses machine learning to predict student academic performance using the UCI Student Performance dataset. The goal is to classify students as either Pass or Fail based on their final grade.

For this project, students with a final grade of 10 or higher are classified as Pass, while students with a final grade below 10 are classified as Fail. This project is intended to explore how machine learning could be used as an early warning tool to help identify students who may need additional academic support.

## Dataset

The dataset comes from the UCI Machine Learning Repository Student Performance dataset. It includes academic, demographic, and school-related features such as study time, absences, previous grades, family background, and school support.

The Portuguese language course dataset was used. It contains 649 rows and 33 columns. There were no missing values in the dataset.

## Tools and Libraries

This project was completed in Python using Google Colab.

Libraries used include:

- pandas
- numpy
- matplotlib
- scikit-learn

## Models Used

Three supervised learning models were trained and compared:

- Logistic Regression
- Decision Tree
- Random Forest

The models were evaluated using accuracy, precision, recall, F1-score, and a confusion matrix.

## Results

The Random Forest model had the highest validation F1-score and was selected as the final model.

Final test results:

- Accuracy: 0.8538
- Precision for Fail: 0.52
- Recall for Fail: 0.65
- F1-score for Fail: 0.5778

The confusion matrix showed that the model correctly predicted 13 failing students and 98 passing students. It incorrectly predicted 7 failing students as passing and 12 passing students as failing.

## Bias and Fairness

This dataset may include bias related to demographic, family, and school-related factors. Because of this, the model should not be used to label or punish students. It should only be used as a decision-support tool to help educators identify students who may need extra support.

The dataset also had class imbalance, with more passing students than failing students. To address this, stratified data splits, class weights, and F1-score were used.

## Overfitting Prevention

To reduce overfitting, the project used:

- Training, validation, and test splits
- Cross-validation
- Maximum depth limits for tree-based models
- Regularization in Logistic Regression

## How to Run the Project

1. Open the notebook in Google Colab.
2. Run all cells from top to bottom.
3. The notebook will load the dataset from the UCI Machine Learning Repository.
4. The models will train and display evaluation results.

## Conclusion

The Random Forest model performed best overall, but it was stronger at predicting students who passed than students who failed. This project shows that machine learning can be useful for educational support, but predictions should always be interpreted carefully and combined with human judgment.
