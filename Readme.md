# Iris Species Classification: A Comparative Study

This project explores the classic Iris dataset through a complete Machine Learning pipeline, comparing Linear, Distance-based, and Tree-based algorithms to find the most robust classifier.

## Executive Summary
- **Top Performer:** Decision Tree & Random Forest (F1-Score: 0.97)
- **Key Insight:** While the 'Setosa' species is linearly separable, 'Versicolor' and 'Virginica' require non-linear boundaries or optimized hyperparameters to distinguish effectively.
- **Methodology:** Implemented 5-fold Cross-Validation and Grid Search to ensure model stability and prevent overfitting.

## Tech Stack
- **Languages:** Python
- **Libraries:** Scikit-learn, Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn (including 3D feature analysis)

## Methodology & Key Findings

### 1. Exploratory Data Analysis (EDA)
I conducted univariate and bivariate analysis, discovering that petal dimensions are the strongest predictors. A 3D scatter plot confirmed significant overlap between Versicolor and Virginica, justifying the use of non-linear models.

### 2. Model Benchmarking
I compared five different algorithms using **Stratified 5-Fold Cross-Validation**:
* **Logistic Regression:** Baseline performance, improved via Polynomial Features (Basis Functions).
* **K-Nearest Neighbors (KNN):** Optimized $k$ via Grid Search.
* **Decision Tree & Random Forest:** Analyzed feature importance; these models provided the highest precision and recall for overlapping classes.

### 3. Evaluation Metrics
Beyond simple accuracy, I evaluated models using:
- **Confusion Matrices:** To pinpoint exactly where species were being misclassified.
- **F1-Scores:** To balance Precision and Recall for medical-grade classification scenarios.
- **Box Plots:** To visualize the variance and reliability of each model across data folds.

## Conclusion
The **Tree-based models** outperformed others due to their ability to create non-linear "rectangular" decision boundaries that better isolate the overlapping feature space of the Virginica species.