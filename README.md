The lab focuses on implementing and comparing Linear SVM and RBF (Radial Basis Function) SVM models for predicting machine failure using the AI4I 2020 Predictive Maintenance Dataset.
Dataset
Dataset: AI4I 2020 Predictive Maintenance Dataset
Total records: 10,000
Input features:
Type
Air Temperature (K)
Process Temperature (K)
Rotational Speed (rpm)
Torque (Nm)
Tool Wear (min)
Target: Machine Failure (0 = No Failure, 1 = Failure)
Preprocessing
Data split into:
80% Training (8,000 samples)
20% Testing (2,000 samples)
Applied:
OneHotEncoder for categorical feature (Type)
StandardScaler for numerical features
Combined using ColumnTransformer in a machine learning pipeline.

Linear SVM Results
Accuracy: 96.95%
Precision: 0.00
Recall: 0.00
F1-Score: 0.00

Observation: Although the model achieved very high accuracy, it failed to detect any machine failures. 
Due to class imbalance, the classifier predicted all instances as "No Failure", making it ineffective for failure prediction

RBF SVM Results
Accuracy: 97.7%
Precision: 85.71%
Recall: 29.51%
F1-Score: 43.90%

Confusion Matrix Results:
True Negatives: 1936
False Positives: 3
False Negatives: 43
True Positives: 18

Comparison
Metric-inear SVM-RBF SVM
Accuracy-	96.95%-97.70%
Precision-0.00-85.71%
Recall-0.00-29.51%
F1-Score-0.00-43.90%

Conclusion

The Linear SVM suffered from the dataset's class imbalance and failed to identify any failure cases. 
In contrast, the RBF SVM successfully detected machine failures and achieved better Precision, Recall, and F1-Score. Therefore, RBF SVM is the better model for predictive maintenance and machine failure detection on the AI4I 2020 dataset.
