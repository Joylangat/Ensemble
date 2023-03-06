Columns and definitions are described below.

Age — the age of the policyholder.
Gender—Gender of the policyholder (female, male).
BMI – Body Mass Index provides an understanding of the body, weight relatively high or low relative to height, an objective measure of weight using height-to-weight ratio (kg/m^2), ideally 18, 5-25
Children — The number of children/dependents of the policyholder. Smoker — Policyholder's smoking status
Region – The policyholder's region of residence in the United States
Fees – Individual medical expenses charged by health insurance.

For the insurance info 
The summary is:
         There are 1,338 insurance records with 7 variables.
         The data set does not have any null or missing values.
         There are categorical and numerical data types. 
In the insurance description:
          The average age is 39 years.
          The average body mass index is 30.66.
          The average number of children is 1.
          The average claims charge was $13,270.
The bar graphs in the output of the code represents visualizing the relationship between the age,  gender, the body mass index, the number of children, the smoker/non-smoker and the region against the claim charge. The observations are as follows: 
Claims premiums gradually increase with age.
Claims fees are slightly higher for men.
As the body mass index rises, the damage award increases. Interestingly, the injury cost for the BMI 40-45 group decreases slightly.
If 2 or her 3 children are covered by insurance, the bill will be higher. Billing fees are significantly higher among smokers.
Damage charges are similar in all regions, with the Northwest having the highest charges.          
Then we get to check the charges column for variances in the values given. Values for variable charges vary widely. 
Visualization of the distribution of claim charges. The price values are skewed to the right side of the axis. Use sklearn's min and max scaling to normalize the charges. This converts the price values to a range of 0 to 1, making it easier for the model to process the data.
Selecting of features. I need to convert categorical data to numeric data. This conversion uses one-hot encoding. One Hot Encoding is a technique that replaces categorical data with binary numbers. The transformed column is given a number corresponding to the value. 
Use Pearson's correlation method to create a correlation matrix that measures the linear association between the characteristic and the target variable. The observations are: There is a strong correlation between smokers and charges, there is a weak correlation between age and charges and there is a weak correlation between BMI and charges.
Gender and region characteristics are of minimal value for this analysis and should be removed. Since BMI is already in the dataset, we also remove the BMI class feature. 
Spliting the data into training and test datasets. First, we need to divide our data into x values (the data we will use to make predictions) and y values (the data we are attempting to predict).We will use the train_test_split function to generate training data and test data. The test data set will include 25% of the original data set.
Normalizing the data. We need to normalize the data so that its distribution will have a mean value of 0 and a standard deviation of 1. Normalization makes the features more consistent with each other, which allows the model to predict outputs more accurately. This is done for each feature or column in the data set.
Measure model performance using the root mean squared error (RMSE). Square root means the squared error is a metric that gives the average distance between the predicted value from the model and the actual value in the dataset. RMSE is calculated by computing the residual (the difference between the predicted and the true) for each data point, computing the norm of the residual for each data point, computing the mean of the residuals, and taking the square root of the mean. increase. The lower the value, the better the model's performance. 
