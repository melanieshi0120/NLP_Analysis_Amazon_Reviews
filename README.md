# NLP_Analysis_Amazon_Reviews
![ceo.jpeg](ceo.jpeg)
## Goal: 
Using Amazon data to predict if the review is negative or positive
- If rating <=3  negative review  0
- If rating >=4  positive review  1
## Attribute information
1.  helpful - helpfulness rating of the review [2,3], e.g. 2/3 ,  2 is numerator , 3 id denominator
            Numerator: Number of readers who found the review is  helpful
            Denominator: Number of readers who indicated whether they found the review helpful or not.
2. review Text - text of the review
3. overall - rating of the product
4. summary - summary of the review
5. unix Review Time - time of the review (unix time)
## EDA
![bigram.png](bigram.png)

## Data cleaning and preprocessing
1. Combined summary column and review column as “combined_text”
2. Created a target column based on rating column 
3. Created two columns, one is helpfulness_numerator ,another one is helpfulness_denominator 
4. Tokenization, Punctuation removal , stemming, lemmatization 
5. After step 4.  created a column - review_len which is length of review(text)
6. Data Resampling (Oversampling Method)

## Modeling
There are two part at first level, text data analysis and non_text data analysis. For text data , Naive Bayes Classifier, Neural Network and Logistic Regression were applies and obtianed each model's preditions (train data and test data ). For the non_text data, Ramdon Forest , Neural Network and Logistic Regression were applied and generated the predictions. At second level, All six train-data preditions  and six test-data prediction were combined as new features renamed as  new x_train data and new x_text data. XGboost and Neural Network were applied to predict again. 
![overall_process.png](overall_process.png)








## Presentation:https://docs.google.com/presentation/d/1pjb43sTBqI7z4jKIwuu9FlcUvjYyJvtK07uPGz71drQ/edit?usp=sharing
## Dashboard:https://public.tableau.com/profile/hua.shi#!/vizhome/NLPAnalysiswithAmazonSportsOutdoorReviewData/Dashboard1?publish=yes
