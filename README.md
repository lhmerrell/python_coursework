Diabetes (scikit.learn)

This Jupyter notebook is designed to descriptively analyse and then run predictive models on diabetes data from 442 participants. The code is largely generic and could be applied to other datasets with one target variable and many predictors. However, care must be taken when choosing the most appropriate type of regression model and therefore code may be added/removed to best fit the data.

To run: 

1. The core modules are at the top of the notebook, with additional modules found at relevant points 
throughout the notebook. 
2. A separate data file is not needed for import as the URL for the dataset from 
scikit.learn is embedded in the code "https://www4.stat.ncsu.edu/~boos/var.select/diabetes.tab.txt". 
Whilst the variable names could be changed in the .tab file, it is best for repeatability to use those 
presented.
3. The obesity filters were based on BMI thresholds found at 
https://www.nhs.uk/conditions/obesity/
4. The descriptive analyses of this data are entirely subjective 
and therefore could be set to categorise based on any of the other systemic markers of diabetes e.g., 
hyperglycemia (increased blood sugar level) or hypertriglyceridemia (increased triglyceride 
concentrations). 
5. When running the simple linear regression models be aware of changing the attribute 
(Attr) to ensure the attribute of interest is substituted into the simple model. Users may wish to change 
whether the intercept is fixed, but this is set to True as default, as is the split of train/test data 
(75/25). I found no single variable to strongly predict diabetes progression one year after baseline. 
6. Moving on to a multiple linear regression, again variables can be substituted into the model as desired, 
and the intercept is fixed as default. Four predictive variables were selected here due to their 
physiological relevance to diabetes however the model score was not satisfactory.
7. When assessing the collinearity heatmap for predictive variables, it became evident that a ridge regression model may be 
more appropriate than a linear regression. It may be here that users with other data do not see 
collinearity, and the assumptions of a multiple linear regression have not been violated. 
8. If, as in this instance, there is collinearity between predictive variables, running a ridge regression may be a 
more robust statistical method. When finding the best alpha value to use in the regression, the searching 
intervals can be manipulated with more or less intervals between the chosen range of values i.e., (0, 10, 100) denotes 100 values between 0 and 10.

Whilst this code is simplistic, it may be useful for beginners to become familiar with Python language and complete descriptive data analysis and statistical modelling. The code can be applied to a range of data, but users should follow the narrative of the analysis and adjust parameters where necessary to best fit the data of interest.

Acknowledgements: With thanks to Matt Williams (https://milliams.com/courses/) and Callum Young (fellow SWBio DTP Student) for their help and sharing their code.


