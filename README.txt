This project features the data analysis of "Sleep Health and LifeStyle Dataset" from Kaggle https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset/data to make a predictive model of sleep disorders. The motive for this project is further substantiated by this research paper that concluded that poor sleep is a national public health issue that needs to be looked into. 

#Data Preparation and Cleaning 
We looked into a total of 8 predictors which includes : gender, age, occupation sleep duration, quality of sleep, physical activity level, stress levels, BMI category, blood pressure, heart rate, daily steps and how they affect presence of sleep disorders specifically sleep apnea and insomnia. 

Through data cleaning, we removed null values, duplicates, irrelevant columns and poorly represented categories. We also merged similar categories and slit blood pressure into systolic and diastolic pressure to calculate each individual’s blood pressure category based on this guideline.[the guideline, a reference]

Using the cleaned dataframe, we intended to use the insights gained from EDA to identify the top three predictors for the machine learning models.[pic of cleaned dataframe]

##Univariate Analysis
-1.Univariate analysis showed not much of a pattern to be observed except for some negative and positive skew.
-2.The distribution of gender, BMI category, blood pressure category are also quite self-explanatory.
-3.The distribution of occupation shows a majority of nurses, doctors, and engineers.
-4.The distribution of sleep disorders also shows the ratio of not having a sleep disorder to having one is 58.5% to 41.5% which makes analysing predictors related to sleep disorder a feasible problem statement.

##Bivariate Analysis
-1.Age and Sleep Disorder
-2.Sleep duration and Sleep Disorder
-3.Gender and Sleep Disorder
-4.Occupation and Sleep Disorder
-5.BMI Category and Sleep Disorder
Quality of sleep, physical level, stress level, heart rate, number of daily steps and blood pressure category are determined to be bad predictors as some of them are either missing median lines, IQR boxes, showing no correlation or contain anomalies.




#MODEL : 

After analysisng which predictors have stronger correlations based on EDA and feature importance of each predictor, 4 models were made using different combinations of the predictors: 
            Model 1. Occupation, Sleep Duration, BMI Category
            Model 2. BMI Category, Age, Daily Steps
            Model 3. Occupation, Sleep Duration, Daily Steps 
            Model 4. BMI Category, Age, Gender  

And for each model, we did the following : 
    - 1. Create a model (depth=3,n_estimators=100) using RandomForest method first
    - 2. We further tuned the parameters (max_depth and n_estimators) using GridSearch method      
    - 3. We built a post-tuning model using RandomForest method 



#RESULT : 
 (copy the slide) 

Model 3 is the best predictive model as it has the highest post-tuning test accuracy and the cross validation score of 0.9189 and 0.8991(Figure 2). The cross-validation scores indicate how well a machine learning model generalises to unseen data by testing it on multiple subsets while post-tuning test accuracy reflects the model's performance after hyperparameter optimisation. Thus, model 3 is able to provide reliable predictions for practical uses. 

From the model, we can conclude that the 3 best predictors for sleep disorders is sleep duration, daily steps and occupation. Though occupation is not something we would think of as reasons for sleep disorders are usually associated with biological and lifestyle choices, it still ended up as a strong predictor for sleep disorders highlighting the influence work has on our lives. Our conclusion is one can possibly prevent sleep disorders to improve quality of life is through having longer hours of sleep and engae in daily exercise. 








