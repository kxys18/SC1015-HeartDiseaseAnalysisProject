## Welcome to Heart Disease Analysis Project!
### About
This is a mini project for SC1015-Introduction to DSAI.

Our team's objective is to make use of [Cardiovascular-Diseases-Risk-prediction-dataset](https://www.kaggle.com/datasets/alphiree/cardiovascular-diseases-risk-prediction-dataset) to look at various lifestyle choises and predict whether a person has heart disease or not.
Please view the source code in order from:
1. [Data Cleaning and EDA](EDA.ipynb)
2. [Decision Tree Model](DecisionTree.ipynb)
3. [K-nearest Neighbours](KNN.ipynb)
4. [Naive Bayes Classifier](NaiveBayesClassifier.ipynb)
5. [Random Forest](RandomForest.ipynb)

### Problem Rationale
- Heart and circulatory diseases account for approximately 1 in 3 global deaths. This results in an estimation of 20.5 million fatalities in 2021. This would also mean an average of 56,000 deaths per day, or one death every 1.5 seconds, which makes cardiovascular diseases the leading cause of mortality worldwide. With the global number of deaths from heart diseases predicted to rise in the future, it is important to take preventive measures that ensure global well-being. Hence we decided to work on this topic.

### Problem Definition
- Given a person's lifestyle choices such as Smoking_History and basic information such as BMI, are we able to predict whether the person is likely to have heart disease?

- Which model would be the best to predict it?

### Data Preparation and Cleaning
- Check for duplicates
- Remove deplicates
- Drop Columns such as 'Other_Cancer' that we have less information on
- Rename columns (Eg. 'Weight_(kg)' to 'Weight' for easier access)

### Exploratory Data Analysis
- Create visualisations for both univariate and bivariate analysis
- Decided to use Kendall’s Tau over Pearson correlation. It is able to handle deviations from perfect patterns, and our dataset comprises a mix of numerical data and categorical variables, including ranked and unordered categories. Kendall's Tau accommodates both ranked and unranked data, making it more suitable for our diverse dataset, unlike Pearson, which assumes linear relationships.

### Models Used
1. Decision Tree 
2. KNN
3. Naive Bayes Classifier
4. Random Forest
-   We also explored further and improved our models, where for KNN model we tried applying downsampling and random oversampling to reduce the effect the imbalanced data had on the model’s result, while for random forest, we tried customized voting system and found the threshold of voting system with better performance.
With this, our project can predict whether someone is likely to have heart disease given their basic lifestyle choices. 


### Data Driven Insights and Conclusion
- Looking at RandomFOrest and Naive Bayes, we can see that while the threshold is 4, the Random Forest Model has approximately the same recall rate of 1 class while the overall accuracy is larger than Naive Bayse's result with a difference of 2.5% which shows than random forest is a better model in this case.
- We also found that, In an imbalanced data set, the classifier tends to predict the testing data as the case of the majority group. When we are focusing on the minority group like people with heart disease in our project, this may bring trouble. In the future, we can study the theoretical explanation of why an imbalanced data makes the classifier more likely to return the majority case and try to establish a more effective model to work on imbalanced data. 

### Contribution
- Angelina Joanne Solomon: EDA, Decision Tree
- Krystal Pek Ke Yun: EDA, KNN
- Liu Xiaotao: Decision Tree, Naive Bayes Classifier, Random Forest

### Refences
- Jackson, P. C., & Woolridge, M. J. (Second Edition). Introduction to Artificial Intelligence.
-  https://www.who.int/health-topics/cardiovascular-diseases#tab=tab_1
- https://www.geeksforgeeks.org/python-kendall-rank-correlation-coefficient/

- https://www.analyticsvidhya.com/blog/2018/03/introduction-k-neighbours-algorithm-clustering/

- https://machinelearningmastery.com/random-oversampling-and-undersampling-for-imbalanced-classification/