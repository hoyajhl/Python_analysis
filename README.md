# Python_analysis
### Dementia_prediction
Data sources: MRI and Alzheimers Magnetic Resonance Imaging Comparisons of Demented and Nondemented Adults
Dataset: 

-Cross-sectional MRI Data in Young, Middle Aged, Nondemented and Demented Older Adults: 
This set consists of a cross-sectional collection of 416 subjects aged 18 to 96. 
For each subject, 3 or 4 individual T1-weighted MRI scans obtained in single scan sessions are included. The subjects are all right-handed and include both men and women.
100 of the included subjects over the age of 60 have been clinically diagnosed with very mild to moderate Alzheimer’s disease (AD). 
Additionally, a reliability data set is included containing 20 nondemented subjects imaged on a subsequent visit within 90 days of their initial session.

-Longitudinal MRI Data in Nondemented and Demented Older Adults: 
This set consists of a longitudinal collection of 150 subjects aged 60 to 96.
Each subject was scanned on two or more visits, separated by at least one year for a total of 373

Purpose: Estimating the CDR (scale of Dementia) using relevant features in the MRI dataset

Analysis Flow 
``` 
Drop all the rows with undefined or null values
Removing columns (unnecessary for our analysis)

Imputation using simpleImputer
-Fill in the missing values in the "SES" columns with the most occuring data element.
-Fill the missing values in the "MMSE" column with the median of that column.

Encoding the Target variable using LabelEncoder
Converting categorical variables to numeric using OneHot encoding

Hyperparameter tuning using cross-validation for XGB and compare with gradient boosting model 
Restore xgb model based on best estimator parameter tuning
```

References
https://www.kaggle.com/jboysen/mri-and-alzheimers
