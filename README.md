# Team_Yellow
![](Images/wine.png)

# White Wine and Red Wine Quality

# Backgroud
>The two datasets are related to red and white variants of the Portuguese "Vinho Verde" wine.
>For more details, consult: http://www.vinhoverde.pt/en/ or the reference [Cortez et al., 2009].
>Due to privacy and logistic issues, only physicochemical (inputs) and sensory (the output) variables
>are available (e.g. there is no data about grape types, wine brand, wine selling price, etc.).

>These datasets can be viewed as classification or regression tasks.
>The classes are ordered and not balanced (e.g. there are munch more normal wines than
>excellent or poor ones). Outlier detection algorithms could be used to detect the few excellent
>or poor wines. Also, we are not sure if all input variables are relevant. So
>it could be interesting to test feature selection methods.

## Reason the topic was selected
The Global Market value of Wine has reached over $340 billion dollars and continue to grow. If we can determine which elements have the greatest impact on the quality of wine, we can provide a good indication on how the wine will sale and improve quality assurance. Also, wine is delicious and a staple in any household.

# Description of the source of data
The data was downloaded from Kaggle: https://www.kaggle.com/datasets/danielpanizzo/wine-quality
It came as a two CSV file White Wine with 4899 rows and 12 columns and Red Wine with 1600 rows and 12 columns.

*Columns*
Input variables (based on physicochemical tests):
1 - fixed acidity (tartaric acid - g / dm^3)
2 - volatile acidity (acetic acid - g / dm^3)
3 - citric acid (g / dm^3)
4 - residual sugar (g / dm^3)
5 - chlorides (sodium chloride - g / dm^3
6 - free sulfur dioxide (mg / dm^3)
7 - total sulfur dioxide (mg / dm^3)
8 - density (g / cm^3)
9 - pH
10 - sulphates (potassium sulphate - g / dm3)
11 - alcohol (% by volume)
Output variable (based on sensory data):
12 - quality (score between 0 and 10)
# Technologies Used (Renata Lemos)
Slack - main communication tool.
Python/Pandas - ETL ,matplotlib
Jupyter lab - run notebooks
Github - to host data and facilitate communication and collaboration between team members.
PostgreSQL - to create the Database on AWS.
Tableau - Create and style worksheets, dashboards, and stories in Tableau.

## Data Cleaning and Analysis
Pandas will be used to clean the data and perform an exploratory analysis. Further analysis will be completed using Python.
# Description of the data exploration phase of the project
- Make sure there is no null values
- No duplicates
- Make sure all data is in object intenger
- Calculating the variance of each element
- Formatting the numbers

## Database Storage (Ashley Gaddis)
PostgreSQL Database on AWS is the database we intend to use, and we will integrate Tableau to display the data.

## Machine Learning (Amanda Cancio)

### Supervised Machine Learning
- Create training and test groups from a given data set.
- The data was first cleaned, explored, and scaled, and then run through a Radom Forest Classifier.
- Implement the random forest.
- Compare the advantages and disadvantages of each supervised learning algorithm.
- Determine which supervised learning algorithm is best used for a given data set or scenario.
- Use ensemble and resampling techniques to improve model performance.
- SciKitLearn is the ML library we'll be using to create a classifier.

SciKitLearn is the ML library we'll be using to create a classifier.  The data was first cleaned, explored, and scaled, and then run through a Radom Forest Classifier.


# Description of the analysis phase of the project
- Ranking the elements (elements name
- Determining if there is any corrolation between the elements
# Technologies, languages, tools, and algorithms used throughout the project
- Train test split
Python:
- Create an ETL pipeline from raw data to a SQL database.
- Clean and transform data using Pandas.
- Load data with PostgreSQL.

- Standard Scaler 
- Clustering ( to determine the 5 most important elements 
- Oversampling and Undersampling to balance the data set

## Dashboard
In addition to using a Tableau , we will also integrate D3.js for a fully functioning and interactive dashboard. It will be hosted on ___.

## Questions the team hopes to answer with the data
- Which elements have a greater impact on the quality of wine?
- Does the type of wine affects the elements that have a greater importance?
- Is the machine learn model applicable to other types of wine?
### Additional questions that will need to be further analyzed. 
- Can those elements be manipulated to assure the quality of the wine?
- What affects the elements that determine the quality of the wine?

# What knowledge do we hope to glean from running an unsupervised learning model on this dataset?
We can group elements together based on how each element affects the final quality of the wine.
Which white wine has the best quality and what elements affect the quality of the wine?
