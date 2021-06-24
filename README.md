# REF-UoA11-Ontology



The turtle file (.ttl) contains the full design of the REF2014 UoA-11 Computer Science and Informatics Ontology. The file only provides approximately 50% of the original data, which contains the entities and the corresponding attribute data for the entity.



The .csv file contains the flatten form of the 125 selected impact case studies within the 'Low Variance Threshold'. This include: 

* 7 UoA features

* 38 Case study features that were extracted from the text
* Estimated score for each impact case study in 5-point sacle (integer from 0-4) and 9-point scale (half-integer and integer from 0-4).



## Reproducibility Statement
Methods and settings to reproduce the paper’s main results in grade prediction: imbalanced-learn implementation of ADASYN, XGBoost, Scikitlearn implementations of SVM and grid searches with cross validation of the following parameter spaces:

Use of SMOTE in 5-class classification: Sampling strategy: {0:12, 1:18, 2:60, 3:55}, n_neighbour = 4
1. XGBoost regressors: Maximum depth: 1,2,3,4; Minimum child weight:1,2; subsample:0.6, 0.7, 0.8, 0.9; Colsample_bytree:0.6, 0.7, 0.8, 0.9; Number of estimators: 100, 200, 300, 400, 500; learning rate: 0.05, 0.06, 0.07, 0.08, 0.09.
2. 3. XGBoost classifiers: Maximum depth: 2,3,4; Minimum child weight:1,2; subsample:0.6, 0.7, 0.8, 0.9; Colsample_bytree:0.6, 0.7, 0.8, 0.9; Number of estimators: 100, 200, 300, 400, 500; learning rate: 0.05, 0.06, 0.07, 0.08, 0.09.
3. SVM regressors: Kernel: linear, rbf, sigmoid; coef0: 0, 0.01, 0.03, 0.05; Degree: 1, 2, 3, 4, 5; gamma:1, 2, 3; C: 0.1, 1, 3, 5, 7, 10. 
4. SVM classifiers: Kernel: linear, rbf, sigmoid; coef0: 0, 0.01, 0.03, 0.05; Degree: 1, 2, 3, 4, 5; gamma:1, 2, 3; C: 0.1, 1, 3, 5, 7, 10. 

