# gtc-ml-project1-hotel-bookings
data cleaning, EDA and preprocessing project  

This repository contains a Jupyter Notebook that performs an exploratory data analysis (EDA), data cleaning, feature engineering, and preprocessing on a hotel booking dataset to prepare it for predictive modeling.

Dataset
The dataset used in this notebook is hotel_bookings.csv, which contains information about hotel bookings, including booking details, guest information, and booking status.

Notebook Contents
The notebook covers the following steps:

Exploratory Data Analysis (EDA) & Data Quality Report: Initial examination of the data, including displaying the head of the DataFrame, checking data types and non-null counts (.info()), examining the shape of the data, generating descriptive statistics (.describe()), checking for missing values, visualizing missing values using a heatmap, and identifying key numerical columns for outlier detection.
Data Cleaning:
Calculating IQR for numerical columns to identify outliers.
Filtering the DataFrame to remove rows with outliers based on the IQR.
Dropping duplicate rows.
Checking for remaining missing values after outlier and duplicate removal.
Converting boolean columns to boolean type.
Filling missing values in 'children', 'agent', 'company', and 'adr' columns with 0 and converting them to integer type.
Filling missing values in the 'country' column with 'unknown'.
Feature Engineering & Preprocessing:
Examining unique values in categorical columns.
Creating new features:
total_guests: Sum of 'adults', 'children', and 'babies'.
total_nights: Sum of 'stays_in_weekend_nights' and 'stays_in_week_nights'.
arrival_date: Combining year, month, and day columns into a datetime object.
is_family: A binary feature indicating if the booking includes children.
Applying one-hot encoding to selected categorical features (hotel, meal, market_segment, distribution_channel, deposit_type, customer_type, reservation_status).
Applying frequency encoding to the 'country' column.
Applying ordinal encoding to the 'reserved_room_type' and 'assigned_room_type' columns.
Dropping the original 'reservation_status' and 'reservation_status_date' columns.
Splitting the data into training and testing sets for the target variable 'is_canceled'.
How to Run the Notebook
Clone this repository to your local machine.
Make sure you have Jupyter Notebook or JupyterLab installed.
Install the required libraries: pandas, numpy, matplotlib, seaborn, sklearn.
