# MSC Business Analytics Project - GUI Application Documentation

## Overview

This PyQt5 GUI application provides a pipeline for classification model development in a business analytics context. It allows users to upload datasets, preprocess data, perform feature scaling, handle outliers, split data, resample to handle class imbalances, and train various machine learning models. The application includes visualization and evaluation features, displaying model performance metrics to help users select the best model for their classification problem.

---

## Table of Contents

- [1. Imports](#1-imports)
- [2. GUI and Main Window Setup](#2-gui-and-main-window-setup)
- [3. File Handling and Data Preview](#3-file-handling-and-data-preview)
- [4. Data Preprocessing](#4-data-preprocessing)
  - [scaleData](#scaledata)
  - [treatOutliers](#treatoutliers)
  - [splitData](#splitdata)
- [5. Data Resampling](#5-data-resampling)
- [6. Model Training and Evaluation](#6-model-training-and-evaluation)
  - [Evaluation Plots](#evaluation-plots)
- [7. Results Display](#7-results-display)
- [8. Error Logging](#8-error-logging)
- [9. Execution](#9-execution)
- [Summary of Usage](#summary-of-usage)

---

## 1. Imports

The application uses the following libraries:

- **PyQt5**: For building the GUI components.
- **Scikit-learn**: Provides machine learning models, preprocessing tools, and evaluation metrics.
- **Imbalanced-learn**: Includes sampling techniques for imbalanced datasets.
- **Matplotlib & Seaborn**: Used for plotting evaluation metrics.
- **Pandas & Numpy**: For data manipulation and numerical operations.
- **SciPy**: Utilized for statistical functions.

---

## 2. GUI and Main Window Setup

### `Main(QMainWindow, Ui_MainWindow)`

The `Main` class is the primary window of the application. It initializes the GUI components and connects each button to its respective function.

**Main Functionalities Provided**:

- **File Handling**: Allows users to upload a CSV file and preview its content.
- **Instructions**: Displays a message box with instructions on how to use the application.

---

## 3. File Handling and Data Preview

- **`upload_button_function`**: Opens a file dialog to upload a CSV file, which is loaded into a pandas DataFrame and displayed in a `QTableWidget`.
- **`previewData` and `previewData_pre_process`**: Display previews of the DataFrame (up to 100 rows) in different tables, either raw data or preprocessed data.

---

## 4. Data Preprocessing

### `scaleData()`
Scales numeric columns in the dataset using `RobustScaler`. If `Amount` and `Time` columns are present, they are also scaled and dropped from the main DataFrame.

### `treatOutliers()`
Handles outliers in specific columns (`V14`, `V12`, and `V10`). For each, it calculates the interquartile range (IQR) and removes values outside the boundaries. If these columns are not present, general outlier treatment is applied to all numeric columns.

### `splitData()`
Splits the dataset into training, validation, and test sets based on user-defined split percentages, using a three-way split.

---

## 5. Data Resampling

### `resampleData()`
Balances class distributions in the training data. Users can choose between:
- **Random Oversampling**: Adds copies of minority class samples.
- **Random Undersampling**: Removes samples from the majority class.

---

## 6. Model Training and Evaluation

The application supports multiple models, each with a dedicated function. The models included are:

1. Logistic Regression (`runLogisticRegression`)
2. Decision Tree (`runDecisionTree`)
3. Random Forest (`runRandomForest`)
4. Gradient Boosted Trees (`runGradientBoostedTrees`)
5. Support Vector Machine (`runSVM`)
6. KMeans Clustering (`runKMeans`)
7. One-Class SVM (`runOneClassSVM`)
8. DBSCAN Clustering (`runDBSCAN`)
9. Voting Classifier (`runVotingClassifier`)
10. Stacking Classifier (`runStackingClassifier`)
11. Label Propagation (`runLabelPropagation`)

Each function:
- Trains the model on the training data.
- Optimizes hyperparameters using `GridSearchCV`.
- Evaluates the model on the test set.
- Logs key metrics (precision, recall, F1, MCC).
- Saves evaluation plots (confusion matrix, ROC, and precision-recall curves) to the working directory.

### Evaluation Plots

Each model generates:
- **Confusion Matrix (`saveConfusionMatrix`)**
- **ROC Curve (`saveROCCurve`)**
- **Precision-Recall Curve (`savePrecisionRecallCurve`)**

The plots are saved as PNG files with unique titles.

---

## 7. Results Display

### `displayResults()`
Displays model results in a table format (`resultsTable`) and highlights the best-performing model based on `MCC` or another specified metric. Details of the top model are also displayed in a text box.

---

## 8. Error Logging

Errors encountered during execution are logged to a file (`msc_project_error_Main_class.log`), enabling easier debugging.

---

## 9. Execution

```python
if __name__ == "__main__":
    # Launches the application

