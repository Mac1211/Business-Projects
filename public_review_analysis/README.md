# Public Review Analysis
The provided Python code performs sentiment analysis on Amazon Echo product reviews. The analysis involves preprocessing the review text, converting it into numerical features, and then training machine learning models to classify reviews as positive or negative based on their sentiment.
## Key Steps and Explanation:
### Import Libraries: 
The code starts by importing necessary libraries for data manipulation, visualization, and machine learning.
### Load Data:
The dataset is loaded from a CSV file into a Pandas DataFrame.
### Data Exploration and Cleaning:
1) The info() method is used to get a summary of the dataset, including column names, data types, and missing values.
2) The describe() method provides descriptive statistics of the numerical columns.
3) A heatmap is used to visualize missing values in the dataset.
4) The hist() function plots histograms for numerical columns to understand their distributions.
The code checks for and handles non-string values in the 'verified_reviews' column, ensuring all reviews are in a consistent format.
5) The length of each review is calculated and stored in a new 'rev_length' column.
6) The 'rev_length' column is plotted as a histogram to visualize the distribution of review lengths.
7) The code identifies and prints the longest and shortest reviews in the dataset.

### Feature Engineering:
1) The dataset is filtered to separate positive and negative reviews based on the 'feedback' column (1 for positive, 0 for negative).
2) The 'rating', 'date', and 'rev_length' columns are dropped as they are not needed for the sentiment analysis.
3) One-hot encoding is applied to the 'variation' column to convert categorical values into numerical features.
4) Punctuation and stop words (common words like 'the', 'and', etc.) are removed from the reviews to clean the text data.
5) CountVectorizer is used to convert the cleaned reviews into a matrix of token counts, where each row represents a review and each column represents a word from the vocabulary.

### Model Training and Evaluation:
1) The dataset is split into training and testing sets.
2) A Multinomial Naive Bayes classifier is trained on the training data.
3) The model's performance is evaluated on both the training and testing sets using a confusion matrix and a classification report, which provide metrics like precision, recall, and F1-score.
4) A Logistic Regression classifier is also trained and evaluated in a similar way to compare its performance with the Naive Bayes model.

#### Overall, this code demonstrates a basic sentiment analysis workflow using machine learning techniques. It can be further enhanced by exploring more advanced text preprocessing methods, feature engineering techniques, and different machine learning algorithms to improve the accuracy and robustness of the sentiment classification.
