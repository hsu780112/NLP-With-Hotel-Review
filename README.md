# NLP-With-Hotel-Review

We are tasked with helping Hotel Management Inc. better understand what qualities of a hotel stay contribute to greater customer satisfaction and higher ratings. For this analysis, we are provided with a large data set consisting of hotel reviews (text fields for positive and negative comments) and details about the stay (hotel location, time & length of stay, etc). Our target column of interest is 'Reviewer_Score' that encodes positive sentiment as 1 and negative as 0.

We will begin with some Exploratory Data Analysis (EDA), and then move into data processing, modelling, and iteration over model improvements.

## Exploratory Data Analysis
First, let's load the data and understand what we are working with.

1. Perform EDA on the data and mention 3-4 observations from which we can draw actionable insights. In our EDA, we may consider creating a data dictionary, basic statistical analysis, data visualizations, data cleaning and preprocessing to prepare the data for modeling.

## Preprocessing
Next, the text data needs to be processed for modelling.

2. Split the data into train and test sets and transform the positive and negative review columns using a CountVectorizer. Consider the following:
- What tokenizer and text cleaning steps do you include?
- Using the vectorizer, maximize the number of features at 500 and make sure that tokens used <10 times are dropped from the vocabulary.
This process may be done on the positive and negative review columns separately and then the resulting arrays merged with the original numeric features to form the final train and test data frames ready for modelling. In our column names, make sure we mark which words are coming from the positive vs negative reviews (we can use a prefix such as pos_ and neg_).

## Modelling
As the data is now ready for modelling, we will be creating two separate models with optimization and evaluation of each.

3. Fit a logistic regression model on the data and analyze the test and train accuracy. Find the top 20 words from the positive reviews that are most predictive of a positive sentiment (Reviewer_Score = 1). Similarly, find the top 20 words from the negative reviews that are most predictive of a negative sentiment (Reviewer_Score = 0). What actionable insights can we draw from these?

4. Using a pipeline, combine PCA with a decision tree classifier.

- Optimize at least 3 hyperparameters including the maximum tree depth and the minimum number of data points required on each leaf node.
- We can use 20 principle components.
- The best parameters should be found using 5-fold cross validation.
Contrast the best results here with the logistic regression model and provide any insights that we may draw from the results.

5. For our best performing model, conduct a more in-depth evaluation by analyzing the confusion matrix and commenting on the model errors and metrics such as precision and recall.
