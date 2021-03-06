
![](Images/wine.png)

# White and Red Wine Quality

### <a href="https://docs.google.com/presentation/d/1lBkx4nlX7K-AxiD_H6Ej8JHxEf8ZiycRnW8QxpIP6WQ/present?slide=id.g124a9435f49_0_10">Google Slides</a>

### <a href="https://public.tableau.com/app/profile/ashley.gaddis2595/viz/WineQuality_16501284766880/ImportantAttributestoDetermineWineQuality3">Tableau Public</a>



-----------------------------------------------------------------------------------

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
“The global Wine Market is estimated to be valued at US$ 513.8 Bn in 2022 and is projected to reach US$ 846.3 Bn by 2032. The overall sales of wine are expected to surge at a CAGR(compound annual growth rate) of 5.1% between 2022 and 2032. The wine market is estimated to account for around ~2% - 4% in alcohol & beverages market.” If we can determine which elements have the greatest impact on the quality of wine, we can provide a good indication on how the wine will sale and improve quality assurance. Also, wine is delicious and a staple in any household.


-------------------------------------------------------------------------------------------------------
## Description of the source of data
The data was downloaded from ![Kaggle](https://www.kaggle.com/datasets/danielpanizzo/wine-quality).
It came as a two CSV files: White Wine with 4899 rows and 12 columns and Red Wine with 1600 rows and 12 columns.

*Columns*
Input variables (based on physicochemical tests):

1. fixed acidity (tartaric acid - g / dm^3)
2. volatile acidity (acetic acid - g / dm^3)
3. citric acid (g / dm^3)
4. residual sugar (g / dm^3)
5. chlorides (sodium chloride - g / dm^3
6. free sulfur dioxide (mg / dm^3)
7. total sulfur dioxide (mg / dm^3)
8. density (g / cm^3)
9. pH
10. sulphates (potassium sulphate - g / dm3)
11. alcohol (% by volume)
*Output variable (based on sensory data):*
12. quality (score between 0 and 10)
-----------------------------------------------------------------------------------------------------
## Technologies Used 
- Slack and Zoom - main communication tool
- Python/Pandas - ETL ,matplotlib, sklearn
- Jupyter lab - run notebooks
- Github - to host data and facilitate communication and collaboration between team members.
- PostgreSQL - to create the Database on AWS.
- Tableau - to display and visualize the data.
- GoogleSlides- for display and presentation tool.

## Data Cleaning and Analysis
Pandas will be used to clean the data and perform an exploratory analysis. Further analysis will be completed using Python.
## Description of the data exploration phase of the project
- Make sure there are no null values
- No duplicates
- Make sure all data is in object intenger
- Calculating the variance of each element
- Formatting the numbers

## Database Storage 
PostgreSQL Database on AWS is the database we intend to use, and we will create a web application with Tableau to display the data from the kaggle website and create a story and dashboard to showcase project.

## Machine Learning 
### Preliminary Data Preprocessing
- Create training and test groups from a given data set.
- The data was first cleaned, explored, and scaled, and then run through a Radom Forest Classifier.
- Implement the random forest.
- Compare the advantages and disadvantages of each supervised learning algorithm.
- Determine which supervised learning algorithm is best used for a given data set or scenario.
- Use ensemble and resampling techniques to improve model performance.
- SciKitLearn is the ML library we'll be using to create a classifier.

    * SciKitLearn is the ML library we'll be using to create a classifier.  The data was first cleaned, explored, and scaled, and then run through a Radom Forest Classifier.
### Preliminary Feature Engineering
- The importance of each feature was determined with the feature_importance_ function.
- The features were then organized in a DataFrame in descending order of importance.
- The DataFrame was graphed as a vertical bar chart.
- The top five features will be focused on in order to evaluate their connection to the quality

### Model Choice
- The data was split into a train-test-split using SciKitLearn.
- The Random Forest Classifier is the preferred model at this stage with the highest accuracy score (68%), although various other models (Easy Ensemble, Random Oversampling, K-Means clustering, etc) were used.
- The original target was then binned using a conditional into two categories, high and low quality
- The Random Forest Classifier's accuracy score improved to 96.4%.
----------------------------------------------------------------------------------------------
## Questions the team hopes to answer with the data

- Which elements have a greater impact on the quality of wine?
- Does the type of wine affect the elements that have a greater impact on the quality of the wine?
- Is the machine learn model applicable to other types of wine?

## Results:

![Quality Dsitribution](Images/quality_distribution.png)
* Most wines were classified at quality 6.
* There is a substantial amount of room for improvement.

![Features Sorted by Importance](Images/bargraph_favoriteFeatures.png)

* Alcohol level is the most important feature when determining the quality of  wine.
* Fixed acidity is the least important feature when determining the quality of wine.

!["Random Forest Classifier"](Images/RFC.png)
* Out of the prediction values 459 values were correctly guessed by the model.
* The model can predict the quality of wine best when the quality is at level 6.
    ** important to note most of the data was labeled as quality 6, this might skew the algorithm

### Random Forest Classifier with Binned Target

![Q Category Distribution](Images/q_category_distribution.png)
* When split into two bins, most wines were in the high quality category.
* High quality is rated 5 or above, while low quality is rated 4 and below.

![CM for binned RFC](Images/CM_for_Binned_RFC.png)
* The confusion matrix after the target output was binned
* This model has high precision and perfect recall for the High Quality category

### Classification Report:

![](Images/Binned_RFC_classification.png)
### Clustering using K-Means

![](Images/elbow_curve.png)

#### 2D 
![](Images/2D_graph_K.png)
#### 3D

![](Images/3D_graph_K.png)

![](Images/3D_graph_K2.png)

### Application to Red Wine
The Machine Learning Model was then applied to a Red Wine dataset, and the results were as follows:

![red_quality_distribution](https://user-images.githubusercontent.com/94088129/165419636-c9399626-6989-43f8-8e86-c30e88e582d3.png)
* More wines in this dataset were classified as 5's
* This data in this dataset is concentrated mainly between the 5's and 6's

![red_features_by_importance](https://user-images.githubusercontent.com/94088129/165418794-063ed42d-10c6-40f2-9d2b-7c3f65e875d0.png)
* Alcohol was still the most important feature in red wines
* Fixed acidity, which was #11 in white wine, is #7 in red wine

![red_RFC](https://user-images.githubusercontent.com/94088129/165419111-6a32d0b9-8dd2-4964-84ee-6dff82dc3383.png)
* The accuracy score for this dataset was 71.5%
* The most accurate prediction was 5, with 6 in second place

![red_binned_CM](https://user-images.githubusercontent.com/94088129/165419347-69a0798d-1519-4cca-afef-4c1f13152880.png)
* Once the target column was binned (0 for low quality, 1 for high quality), the accuracy increased
* The new accuracy score is 96.5%

### Additional questions that will need to be further analyzed. 
- Can those elements be manipulated to assure the quality of the wine?
- What affects the elements that determine the quality of the wine?
