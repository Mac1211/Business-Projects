# Sales Prediction Analysis
The notebook aims to analyze and predict store sales using historical data. The main notebook containing all the analysis and modeling code.
## Dataset
### train.csv: Contains the historical sales data for various stores.

#### Columns:
1) Store: Store identifier
2) DayOfWeek: Day of the week (1 = Monday, 2 = Tuesday, etc.)
3) Date: Date of the record
4) Sales: Total sales for the store on the given day
5) Customers: Number of customers who visited the store
6) Open: Indicator if the store was open (1 = open, 0 = closed)
7) Promo: Indicates if a store-wide promotion was running on that day
8) StateHoliday: Indicates if the day was a state holiday
9) SchoolHoliday: Indicates if the day was a school holiday
10) store.csv: Provides additional information about each store.

### Store.csv
#### Columns:
1) Store: Store identifier (used for merging with train.csv)
2) StoreType: Type of store (e.g., A, B, C, D)
3) Assortment: Assortment level (e.g., a, b, c)
4) CompetitionDistance: Distance to the nearest competitor
5) CompetitionOpenSince: Month and year when the nearest competitor opened
6) Promo2: Indicates if the store is participating in a continuous promotion
7) Promo2Since: When the store started participating in Promo2

### Data Integration
The notebook combines the train.csv and store.csv datasets based on the Store identifier to create a comprehensive dataset that is used for analysis and modeling.

## Analysis and Modelling
The notebook includes the following steps:

1) Importing Libraries and Data: Load essential Python libraries and the datasets.
2) Data Exploration and Cleaning: Inspect and clean the data to ensure it is suitable for analysis.
3) Data Integration: Merge train.csv and store.csv to enhance the dataset with additional store information.
4) Feature Engineering: Create new features and transform existing ones to improve model performance.
5) Data Visualization: Utilize matplotlib and seaborn for creating plots and charts to visualize sales trends and relationships.
6) Predictive Modeling: Implement machine learning models to predict future sales based on the integrated dataset. Prediction is done using Facebook Prophet by importing the prophet library. It gave the good visualization of sales trend for the given period.
7) Model Evaluation: Assess the model's performance using appropriate metrics.

_

