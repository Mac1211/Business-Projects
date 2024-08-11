# Employee Attrition Analysis
This project aims to explore, visualize, and model employee attrition data to identify key factors influencing attrition and to predict which employees are likely to leave the company. The analysis uses a dataset named Human_Resources.csv and employs several data science techniques, including data cleaning, visualization, feature engineering, and predictive modeling.

## Project Workflow
### Data Cleaning and Encoding
Clean the dataset by converting categorical variables to numerical format, dropping irrelevant columns, and visualizing missing values.
1) DataFrame.map(): To convert categorical data to numerical format.
2) sns.heatmap(): To visualize missing values.
3) DataFrame.drop(): To remove unnecessary columns.

### Data Visualization
Visualize the distribution and relationships of different features using histograms, count plots, and KDE plots.
1) DataFrame.hist(): To plot histograms for numerical features.
2) sns.countplot(), sns.kdeplot(): To visualize categorical features and their distribution.

### Data Preprocessing
Preprocess the dataset by encoding categorical features, extracting numerical features, and scaling the data.
1) OneHotEncoder(): To perform one-hot encoding of categorical variables.
2) MinMaxScaler(): To scale features to a given range.

### Exploratory Data Analysis
Perform exploratory data analysis (EDA) to identify patterns and correlations in the data.
1) DataFrame.corr(): To calculate the correlation between features.
2) sns.heatmap(): To visualize the correlation matrix.

### Data Splitting
Split the dataset into training and testing sets for model training and evaluation.
1) train_test_split(): To divide the dataset into training and testing sets.

### Predictive Modeling
I used three methods to do this modelling.
#### Logistic Regression
1) LogisticRegression(): To define and train the logistic regression model.
2) accuracy_score(), confusion_matrix(), classification_report(): To evaluate model performance.

#### Random Forest Classifier
1) RandomForestClassifier(): To define and train the random forest model.
2) confusion_matrix(), classification_report(): To evaluate model performance.

#### Neural Network
1) tf.keras.models.Sequential(): To define the neural network model.
2) model.compile(), model.fit(): To compile and train the model.
3) confusion_matrix(), classification_report(): To evaluate model performance.

### Model Evaluation
Evaluate the performance of each model using confusion matrices and classification reports. Visualize the training history of the neural network.
1) sns.heatmap(): To visualize confusion matrices.
2) plt.plot(): To visualize model loss and accuracy over epochs.

## Conclusion
This project provides a comprehensive analysis of employee attrition using various machine learning techniques. The results can help HR departments identify potential factors leading to employee turnover and take proactive measures to retain valuable employees.
