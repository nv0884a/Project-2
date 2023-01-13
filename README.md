# Project 2  AirBnB: Comparing Seattle and Boston

## Overview of Project

### Case Study on Extract, Transform, Load
   
* Through our data, we aim to look at a comparison of Airbnb data between Seattle and Boston
* We will be exploring the two cities' data by looking at their  listings and reviews
* We used the Extract, Transform, and Load process to to create a unique dataset 
* We created a schemata using PostgreSQL 

Extract:
* Using Kaggle we found and extracted the following data sets:
    * https://www.kaggle.com/datasets/airbnb/boston?select=listings.csv
    * https://www.kaggle.com/datasets/airbnb/boston?select=reviews.csv
    * https://www.kaggle.com/datasets/airbnb/seattle?select=listings.csv
    * https://www.kaggle.com/datasets/airbnb/seattle?select=reviews.csv


Transform:
* Using Jupyter Notebook:
    * Import CSVs
    * Created DataFrames using Pandas
    * Cleaned the DataFrames by deleting columns we found uncessary
    * Merged our datasets Listing and Reviews based on city
    * Created 2 new DataFrames based on merged DataFrame for Boston and the merged DataFrame for Seattle
    * Created 2 new CSV files based on the 2 new DataFrames
    * The new CSV files can be created by running the code in the Data.ipynb file
    * The new CSV files are not in GitHub due to the enormous size of the file 

Load:
* Using PostgreSQL:
    * Created two tables with all of the relevant columns for the two datasets to be imported into databases
    * We ran into some issues when we first imported the data, mainly due to the various numbers of commas that were in the datasets which would cause the import to     fail due to the dataset reading into new columns.
    * We also ran into some issues with some columns being in one dataset and not another, so keeping track of all of the columns was a bit tricky, but we were able to manually remove the commas and additional columns from the CSVs in Excel.
    * Once we had cleaned up the CSVs, we were able to successfully import them into our databases
* This topic was chosen due to insterest we had to learn more about the AirBnB market  
* This data can be used to compare trends through different cities  
* This data allows users to easily search for specifications and reviews for AirBnBs in either Seattle or Boston 
* The final DataFrames and tables and further be merged together if needed to create a new DataFrame to include both Seattle and Boston in the same DataFrame
