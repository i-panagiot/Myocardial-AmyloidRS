# Myocardial Radiomics
This repository provides a method to analyze left ventricle myocardial radiomics from computed tomography (CT) scans.

The script processes and reduces a dataset of myocardial radiomic features to identify variables most strongly associated with extracellular volume (ECV).

Principal Component Analysis (PCA) is performed to standardize and reduce dimensionality, generating both principal components and loadings.

Following PCA, a residualization method is used to remove effects correlated with the mean blood pool HU, standardizing the data and adjusting for residuals. The dataset is further filtered to remove highly correlated features, retaining a smaller, non-collinear subset.

To identify radiomic features with strong associations to ECV, the script calculates and sorts correlations between each radiomic feature and ECV, highlighting the top variables. Finally, Recursive Feature Elimination (RFE) with Random Forest is used to determine the optimal number of radiomic features for predicting ECV, supporting the development of a synthetic radiomic signature.