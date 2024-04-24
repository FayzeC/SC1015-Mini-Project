readme file
- The repo must include a decently composed README file for your TA to read and understand the project.
It is unlikely that your TA will execute your codes for every single project, but they will read the README.
- You may include a copy of your slides that you used in the video presentation (not mandatory) in the repo.
Make sure the README file is decently written (like a short report) to describe your work.
- README does not need to have all minor details, but it should broadly explain your work.
- README does not need to be too huge. Keep it simple, compact, but sufficiently detailed.
- Make sure the README ends with each individual contribution in the project by members.
- Make sure the README ends with each online/offline reference you consulted or utilized.
- Don't go over the top please. Try to make the README a 3 to 5 minute read -- not more.

This project features the data analysis of "Sleep Health and LifeStyle Dataset" from Kaggle https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset/data to make a predictive model of sleep disorders. The motive for this project is further substantiated by this research paper that concluded that poor sleep is a national public health issue that needs to be looked into. 

DATA PREP + EDA 
We looked into a total of 8 predictors which includes : gender, age, occupation sleep duration, quality of sleep, physical activity level, stress levels, BMI category, blood pressure, heart rate, daily steps and how they affect presence of sleep disorders specifically sleep apnea and insomnia. 

Through data cleaning, we 


MODEL : 

After analysisng which predictors have stronger correlations based on EDA and feature importance of each predictor, 4 models were made using different combinations of the predictors: 
            Model 1. Occupation, Sleep Duration, BMI Category
            Model 2. BMI Category, Age, Daily Steps
            Model 3. Occupation, Sleep Duration, Daily Steps 
            Model 4. BMI Category, Age, Gender  

And for each model, we did the following : 
    - 1. Create a model (depth=3,n_estimators=100) using RandomForest method first
    - 2. We further tuned the parameters (max_depth and n_estimators) using GridSearch method      
    - 3. We built a post-tuning model using RandomForest method 



RESULT : 
 (copy the slide) 

Model 3 is the best predictive model as it has the highest post-tuning test accuracy and the cross validation score of 0.9189 and 0.8991(Figure 2). The cross-validation scores indicate how well a machine learning model generalises to unseen data by testing it on multiple subsets while post-tuning test accuracy reflects the model's performance after hyperparameter optimisation. Thus, model 3 is able to provide reliable predictions for practical uses. 

From the model, we can conclude that the 3 best predictors for sleep disorders is sleep duration, daily steps and occupation. Though occupation is not something we would think of as reasons for sleep disorders are usually associated with biological and lifestyle choices, it still ended up as a strong predictor for sleep disorders highlighting the influence work has on our lives. Our conclusion is one can possibly prevent sleep disorders to improve quality of life is through having longer hours of sleep and engae in daily exercise. 








