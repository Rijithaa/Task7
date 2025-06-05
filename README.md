# Task7

Task 7: Support Vector Machines (SVM)
Objective
The goal of this task is to apply Support Vector Machines (SVM) to a binary classification problem, experiment with different kernel types (linear and RBF), visualize decision boundaries, tune key hyperparameters, and evaluate the model using cross-validation.

Dataset Used
We used the Breast Cancer Wisconsin dataset, a widely used dataset for binary classification. It contains 30 numeric features describing characteristics of cell nuclei present in breast cancer biopsies. The target variable indicates whether the tumor is malignant or benign.

Tools and Libraries
Python
Scikit-learn
Pandas
NumPy
Matplotlib

Steps:

1.Loading and Preparing the Dataset
The dataset was loaded using sklearn.datasets.load_breast_cancer. Features were stored in a DataFrame, and the target labels were stored in a separate Series. The data was clean with no missing values.

2.Training SVM Models (Linear and RBF Kernels)
The data was standardized using StandardScaler, and split into training and test sets. Two SVM models were trained:
One with a linear kernel
One with an RBF (Radial Basis Function) kernel
Both models were evaluated based on their accuracy on the test set.

3.Visualization of Decision Boundary
To visualize the decision boundary, we selected two features: mean radius and mean texture. A 2D SVM model with an RBF kernel was trained and its decision boundary was plotted. This provided a clear visual understanding of how the SVM separated the two classes.

4.Hyperparameter Tuning
A grid search using GridSearchCV was conducted to find the best values for hyperparameters C, gamma, and kernel. The best model from the grid search provided improved performance.

5.Cross-Validation for Performance Evaluation
The best-performing model was evaluated using 5-fold cross-validation. This helped ensure that the model's performance was consistent across different subsets of the data and not dependent on a specific train-test split.

Summary
->The linear kernel achieved strong accuracy, but the RBF kernel performed better on this dataset.
->After hyperparameter tuning, the model achieved around 98–99% accuracy.
->Visualization showed clear class separation using non-linear decision boundaries.
->Cross-validation confirmed the model's robustness and generalization.
