# A kNN Model to Predict Benign or Malignant Tumors in Patients Diagnosed With Breast Cancer

This project was initially for my Statistics class, but I later revised and added features to it.
The script found in the Jupyter Notebook performs predictions for finding out whether a tumor in a patient who has been diagnosed with breast cancer is benign or malignant. 

## Description of The Dataset
The dataset can be found here: [Breast Cancer Dataset](https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+%28original%29)

The features in the dataset are:

1. ID Number
2. Clump Thickness: 1 - 10
3. Uniformity of Cell Size: 1 - 10
4. Uniformity of Cell Shape: 1 - 10
5. Marginal Adhesion: 1 - 10
6. Single Epithelial Cell Size: 1 - 10
7. Bare Nuclei: 1 - 10
8. Bland Chromatin: 1 - 10
9. Normal Nucleoli: 1 - 10
10. Mitoses: 1 - 10
11. Class: 2 - Benign, 4 - Malignant

## The Code
To complete this project, I used `pandas`, `seaborn`, `matplotlib`, `numpy`, and `scikit-learn` modules. 

I also needed to polish the data before starting my analysis of it. To do so, I converted the `Class` field to be either a 0 or 1, rather than the original 2/4. 

I also removed all rows with `NaN` values, just to make the analysis easier for myself.

## The Analysis
To start off the analysis, I created a Confusion Matrix using `seaborn` to give myself an idea of which features are the most strongly correlated. 

I then wrote a small loop to find predictions using different nearest neighbor values, and appended all of these prediction percentages to a list. Using `matplotlib`, I plotted these prediction values and chose the nearest neighbor value associated with the highest prediction percentage.

Finally, I performed a k-Fold Cross Validation across my dataset to make sure I was not underfitting nor overfitting my model to my dataset.

Check it out the code in `k-Nearest Neighbors Prediction Model of Breast Cancer Diagnosis from The University of Wisconsin.ipynb`!
