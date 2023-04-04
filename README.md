# Movie Rating Prediction Using Machine Learning

## Table of Contents
1. [Introduction](#introduction)
2. [Data Preparation](#data-preparation)
3. [Exploratory Data Analysis](#exploratory-data-analysis)
4. [Feature Engineering](#feature-engineering)
5. [Model Development and Evaluation](#model-development-and-evaluation)

## 1. Introduction <a name="introduction"></a>
This project aims to predict movie ratings based on user demographics, movie genres, and other relevant features. The GroupLens dataset, which consists of approximately 1,000,209 anonymous ratings of about 3,900 movies made by 6,040 MovieLens users who joined MovieLens in 2000, is used. The dataset is divided into three files: Ratings.dat, Users.dat, and Movies.dat.

## 2. Data Preparation <a name="data-preparation"></a>
The three datasets are imported using pandas, and individual dataframes are created for each. Then, the dataframes are merged using MovieID and UserID as primary keys to create a single Master_Data dataframe. Next, the 'Age' column is modified to categorize users into age ranges based on the given age groups. One-hot encoding is performed for categorical features such as 'Gender' and 'Occupation', and label encoding is applied for 'Zip-code'.

## 3. Exploratory Data Analysis <a name="exploratory-data-analysis"></a>
The dataset is explored using visual representations, such as histograms and bar charts. The following aspects are analyzed:

- User Age Distribution: The distribution of user ages across different age groups is visualized.
- User rating of the movie "Toy Story": The distribution of ratings for the movie "Toy Story" is displayed.
- Top 25 movies by viewership rating: The mean rating for each movie is calculated, sorted by the highest mean rating, and the top 25 movies are visualized using a bar chart.
- Ratings for all the movies reviewed by user 2696: The dataset is filtered for UserID 2696, and the movie ratings are visualized using a bar chart or table.

## 4. Feature Engineering <a name="feature-engineering"></a>
Feature engineering is performed to prepare the dataset for machine learning models:

- Unique genres are identified by splitting the 'Genres' column into a list, flattening the list, and using the set() function.
- A separate column for each genre is created with one-hot encoding using pandas' get_dummies() function.
- The features affecting the ratings of any particular movie are determined by performing correlation analysis or using a feature selection technique (e.g., recursive feature elimination).

## 5. Model Development and Evaluation <a name="model-development-and-evaluation"></a>
Machine learning models are developed to predict movie ratings, and their performance is evaluated:

- The dataset is split into training and testing sets.
- Data normalization/standardization is applied if necessary.
- Different machine learning models (linear regression, decision tree, random forest) are trained to predict movie ratings.
- The models are evaluated using appropriate metrics (mean squared error, R-squared), and the best model is selected based on its performance on the testing set.

Following the above steps, a predictive model is built to estimate movie ratings based on various factors, such as user demographics, movie genres, and other features. This model can be used to recommend movies to users, helping them discover new content tailored to their preferences.
