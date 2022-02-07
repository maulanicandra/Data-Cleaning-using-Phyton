# Data-Cleaning-using-Phyton

Data cleaning on Telco Data is carried out using several methods, namely handle missing values and duplicated rows, outlier management, and feature transformation (numerical and categorical).

In Data Telco, there are several column which are customerID', 'gender', 'SeniorCitizen', 'Partner', 'Dependents','tenure', 'PhoneService', 'MultipleLines', 'InternetService', 'OnlineSecurity', 'OnlineBackup', 'DeviceProtection', 'TechSupport', 'StreamingTV', 'StreamingMovies', 'Contract', 'PaperlessBilling','PaymentMethod', 'MonthlyCharges', 'TotalCharges', 'Churn'], dtype='object.
Step:
1. Find out the data type: TotalCharge Data type is object. TotalCharge needed to be replace to float
2. Find out if there is any potential of duplicated rows: There is no duplicate row
3. Find out if there is Missing Value Information: There is 11 or  missing value information at TotalCharges
4. Describe 'TotalCharges' to find mean, median, std, etc: Since TotalCharges feature has relatively high gap between max and min value and high standard deviation, so its better to transform into categorical. First of all, we should fill the null values with median based on "gender", "SeniorCitizen", "Partner", "Dependents" to shape better pattern of data.
5. Handle outlier: # No outlier found. There is no outlier at "Senior Citizen" because the data is 0 or 1. Therefore, data removal is not needed.
6. Finding unnique value: customerID, tenure, and MonthlyCharges has many unique value
7. Dropping Customer ID, Create Monthly group by 10 groups, Create tenure group by 10 groups
8. Replace all data with yes or no with 0 and 1.
9. One hot encoding to column payment method.
10. Level encoding to 'Contract' and 'InternerService'.
11. Replace high cardinality data "tenure", "MonthlyCharges", and "TotalCharges"
