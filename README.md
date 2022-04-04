# Team_Yellow

# White Wine Quality

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

# Technologies Used
## Data Cleaning and Analysis
Pandas will be used to clean the data and perform an exploratory analysis. Further analysis will be completed using Python.
# Description of the data exploration phase of the project
- Make sure there is no null values
- No duplicates
- Make sure all data is in object intenger
- Calculating the variance of each element
- Formatting the numbers

## Database Storage
AWS___ is the database we intend to use, and we will integrate___ to display the data.

## Machine Learning
SciKitLearn is the ML library we'll be using to create a classifier. Our training and testing setup is ___. Extra ML verbiage here.

# Description of the analysis phase of the project
- Ranking the elements (elements name)
- Determining if there is any corrolation between the elements
# Technologies, languages, tools, and algorithms used throughout the project
- Train test split
- Python
- Pandas
- Standard Scaler 
- Clustering ( to determine the 5 most important elements 
-Oversampling and Undersampling to balance the data set

## Dashboard
In addition to using a Flask template, we will also integrate D3.js for a fully functioning and interactive dashboard. It will be hosted on ___.

## Reason the topic was selected
The Global Market value of White Wine has reached over $340 billion dollars and continue to grow. If we can determine which elements have greater impact on the quality of wine, we can provide a good indication on how the wine will sell and improve quality assurance. Also, wine is delicious and a staple in any household.
# Description of the source of data
The data was download from Kaggle: https://www.kaggle.com/datasets/danielpanizzo/wine-quality
CSV file with 4899 rows and twelve columns.

# Questions the team hopes to answer with the data
# What knowledge do we hope to glean from running an unsupervised learning model on this dataset?
we can group together elements based on how each element affects the final quality of the wine.
Which white wine has the best quality and what elements affect the quality of the wine.
