# 05_matplotlib-challenge

[Pymaceuticals.ipynb](https://github.com/wrighang/05_matplotlib-challenge/blob/main/Pymaceuticals/pymaceuticals.ipynb)

## Background
You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

## Requirements

## Prepare the Data
- Merge the datasets into a single DataFrame
- Display the total number of mice from the merged DataFrame
- Identify each duplicate mouse based on Mouse ID and Timepoint
- Create a clean DataFrame by dropping duplicate mice
- Display the total number of mice from the clean DataFrame

## Generate Summary Statistics
- Calculate the mean of the tumor volume for each regimen using `groupby`
- Calculate the median of the tumor volume for each regimen using `groupby`
- Calculate the variance of the tumor volume for each regimen using `groupby`
- Calculate the standard deviation of the tumor volume for each regimen using `groupby`
- Calculate the SEM of the tumor volume for each regimen using `groupby`
- Create a new DataFrame to store the summary statistics

## Create Bar Charts and Pie Charts
- Generate a bar plot using Pandas to show the total number of timepoints for all mice tested for each drug regimen
- Generate a bar plot using `pyplot` to show the total number of timepoints for all mice tested for each drug regimen
- Generate a pie chart using Pandas to show the distribution of unique female vs. male mice
- Generate a pie chart using `pyplot` to show the distribution of unique female vs. male mice

## Calculate Quartiles, Find Outliers, and Create a Box Plot
- Create a DataFrame with the last timepoint for each mouse ID using `groupby`
- Reset the index of the DataFrame
- Retrieve the maximum timepoint for each mouse
- Define a list of the four treatment groups: Capomulin, Ramicane, Infubinol, and Ceftamin
- Create an empty list to store tumor volume data
- Use a `for` loop to display the interquartile range (IQR) and outliers for each treatment group
- Generate a box plot showing the distribution of final tumor volume for all mice in each treatment group

## Create a Line Plot and a Scatter Plot
- Generate a line plot showing tumor volume vs. timepoint for one mouse treated with Capomulin
- Generate a scatter plot showing average tumor volume vs. mouse weight for the Capomulin regimen

## Calculate Correlation and Regression
- Calculate the correlation coefficient and linear regression model for mouse weight and average tumor volume for the Capomulin regimen

-----------------------------------------------------------------

##CODING_PROCESS

Overall Approach

* I reviewed my notes, PowerPoint slides, and the past PyCitySchools challenge to help guide me through the assignment.

* I looked up how to identify duplicate mice by Mouse ID and Timepoint, then reviewed the code to understand the methods used: duplicate_mice = complete_data_df[complete_data_df.duplicated(subset=["Mouse ID", "Timepoint"], keep=False)]["Mouse ID"].unique()

Summary Statistics 
* I refreshed my understanding of variance and standard deviation to better interpret these statistics. Standard deviation measures how far apart values are in a dataset and variance quantifies how much the values in the dataset vary from the mean. When the data points are close to the mean it suggests a high level of consistnacy within the data set. 

Bar and Pie Charts Section
* I asked the Xpert Learning Assistant and referenced activity materials heavily on this section to understand the differences between Pandas and Pyplot, as well as the methods for creating charts from a Series vs. a DataFrame. To illustrate my understanding, I practiced creating bar and pie charts from both a Series and a DataFrame.
