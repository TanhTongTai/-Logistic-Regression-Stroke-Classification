# Stroke Classification with Logistic Regression

This project is a simple machine learning case study for predicting whether a patient is likely to have a stroke using a logistic regression model. The goal is to explore a binary classification problem, prepare the data, train a model, and evaluate how well it can distinguish between the two classes: stroke and non-stroke.

## Project idea

Stroke prediction is a medical classification task where the model uses patient information such as age, gender, health indicators, smoking status, and other risk factors to estimate the probability of stroke occurrence. Because the target variable is binary, logistic regression is a natural and interpretable choice.

The notebook included in this repository demonstrates the entire workflow from raw dataset exploration to model training and performance evaluation.

## What this project contains

- A Jupyter notebook: `classification-logistic-regression.ipynb`
- This README file with project explanation and usage notes

## Why logistic regression?

Logistic regression is widely used for binary classification because it is:

- easy to understand
- fast to train
- works well for linearly separable patterns in tabular data
- useful for explaining the influence of each feature

Instead of predicting a class directly, the model estimates a probability. For each patient, the model computes a score and passes it through a sigmoid function, producing a value between 0 and 1. If the probability is above a threshold (commonly 0.5), the model predicts the positive class (stroke). Otherwise, it predicts the negative class (non-stroke).

## How the model works

The process is as follows:

1. Data loading
   - Load the stroke dataset from the notebook environment.
   - Inspect the structure of the data and identify important columns.

2. Data cleaning and preparation
   - Check for missing values or invalid entries.
   - Convert categorical variables into numeric form when needed.
   - Define the target variable (stroke label) and feature variables.

3. Feature selection
   - Use the variables that are most relevant to stroke risk prediction.
   - Remove or handle features that do not contribute meaningfully.

4. Train-test split
   - Separate the dataset into a training set and a testing set.
   - This allows the model to learn on one portion and be evaluated on unseen data.

5. Model training
   - Train a logistic regression classifier using the training data.
   - The model learns coefficients for each feature, which show how strongly each factor affects the prediction.

6. Prediction and evaluation
   - Predict stroke labels for the test set.
   - Compare predictions with actual values.
   - Measure performance using classification metrics such as accuracy, precision, recall, F1-score, and confusion matrix.

7. Result interpretation
   - Understand which features contributed most to the risk score.
   - Review whether the model is balanced and whether predictions are reliable for the given task.

## How I did it

The workflow in this project follows a standard data science pipeline:

- observed the dataset and its columns
- checked data quality
- prepared the features for model input
- split data into train/test subsets
- trained logistic regression
- evaluated the result
- documented the findings

This is a common approach for tabular machine learning problems and is especially useful as a beginner-friendly project for learning classification, feature engineering, and model evaluation.

## Typical workflow inside the notebook

The notebook likely follows this structure:

1. Import libraries
   - pandas
   - numpy
   - scikit-learn
   - matplotlib/seaborn for visual analysis

2. Read the dataset
3. Explore the distribution of variables
4. Handle missing data and categorical encoding
5. Build the feature matrix and target vector
6. Train the logistic regression model
7. Generate predictions
8. Evaluate performance
9. Visualize results and interpret the model

## Model interpretation

One of the strengths of logistic regression is interpretability. Each feature has a learned weight, and the sign of that weight helps explain the impact:

- positive coefficient: increases the chance of stroke prediction
- negative coefficient: decreases the chance of stroke prediction

This is useful because it allows us to understand why the model makes certain predictions rather than treating it as a black box.

## Evaluation metrics

The project evaluates the model using common metrics:

- Accuracy: overall percentage of correctly classified examples
- Precision: how many predicted stroke cases were actually stroke cases
- Recall: how many actual stroke cases were correctly identified
- F1-score: balance between precision and recall
- Confusion matrix: summary of true positives, true negatives, false positives, and false negatives

These metrics help assess whether the model is useful in practice and whether it is biased toward one class.

## Example of the decision logic

The logistic regression model does not simply output a label. It estimates the probability of stroke as:

Probability = 1 / (1 + exp(-z))

Where z is a weighted sum of the input features plus a bias term. This makes the output easy to interpret as a risk score between 0 and 1.

## How to run the project

Open the notebook in Jupyter Notebook or Jupyter Lab and run all cells in order:

```bash
jupyter notebook classification-logistic-regression.ipynb
```

If you are using VS Code, you can also open the notebook directly and execute the cells there.

## What I learned from this project

This project helps demonstrate:

- the basics of classification in machine learning
- data preprocessing for tabular data
- how logistic regression models probabilities
- how to interpret evaluation results
- how a simple model can be used as a practical healthcare prediction example

## Summary

This repository is a beginner-friendly logistic regression project for stroke classification. It shows how to go from raw health data to a trained model and a meaningful evaluation. The model is simple, interpretable, and suitable for understanding the fundamentals of binary classification.

If you want, I can also help improve this project by adding:

- a more polished research-style report
- model summary tables
- confusion matrix visualizations
- a cleaned dataset explanation
- a project structure with separate training and evaluation scripts
- a README in a more professional academic format

