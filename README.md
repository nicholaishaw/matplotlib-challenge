# Cancer Drug Analysis Using Pandas and Matplotlib

## Background
Pymaceuticals, Inc., is a fictional pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC)—a commonly occurring form of skin cancer.

As a senior data analyst at this fictional company, I have been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured for each mouse. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked me with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked me for a top-level summary of the study results.

## Analysis Using Matplotlib and Jupyter Notebook
### Dataframe Merging
The study data was contained in two csv files. Using python, we merged the csv files into one dataframe for ease of analysis.

![image](https://github.com/nicholaishaw/matplotlib-challenge/assets/135463220/237b1258-e790-4978-96f5-b8f63676b1d6)

**Figure 1.** *Dataframe importing and merging.*
___
### Summary Statistics
Before any exploratory analyses, we obtained descriptive statistics of tumor volumes for each drug regimen using the aggergate function. In addition, we generated a pie chart showing the sex distribution of the mice using Pandas.

![image](https://github.com/nicholaishaw/matplotlib-challenge/assets/135463220/deb7577a-b860-4f70-ab91-7690b7d2f378)

**Figure 2.** *Descriptive statistics for tumor volume size for each drug regimen.*

![image](https://github.com/nicholaishaw/matplotlib-challenge/assets/135463220/445f51ff-a547-4e77-a6c9-2093aa28c98d)

**Figure 3.** *Bar chart of the count of mouse timepoints for each drug regimen.*
___
### Bar Plot of Timepoints for Each Mouse
In order to examine which drug is more effective, We first used pyplot to create a bar chart to show the average mouse lifespan for each drug regimen

![image](https://github.com/nicholaishaw/matplotlib-challenge/assets/135463220/92ab25a5-3e7c-44c5-8863-53d3442649cc)

**Figure 4.** *Bar chart illustrating the average mouse survival in each drug regimen.*
___
### Boxplot Analyses
Using a box plot analysis with matplotlib, We acquired the tumor volume (mm3) distribution of our primary drugs of interest: Capomulin, Ramicane, Infubinol, and Ceftamin. We also used a for loop statement to identify any potential outliers and marked them on the graph.

![image](https://github.com/nicholaishaw/matplotlib-challenge/assets/135463220/f0d588e8-9f7b-46e7-8b3d-4b9b0844972e)

**Figure 5.** *Python script to identify outliers.*

![image](https://github.com/nicholaishaw/matplotlib-challenge/assets/135463220/ddd53236-25f7-4afa-9cf5-e1f35571f9b0)

**Figure 6.** *Box plot that shows the distrubution of the tumor volume for each treatment group and any outliers.*
___
### Linear Regression
Finally, using a linear regression, we investigated the association between tumor volume (mm3) and mouse weight for mice given Capomulin. The linear regression demonstrated a significant positive association between tumor size and weight (*p* = 1.322e-07, *r* = 0.84)

![image](https://github.com/nicholaishaw/matplotlib-challenge/assets/135463220/ea80beb9-f07b-4c70-9c65-bf68c4aea704)

**Figure 7.** *Linear regression of tumor volume and mouse weight*

![image](https://github.com/nicholaishaw/matplotlib-challenge/assets/135463220/08ab0d23-ca3f-41b3-8b5c-53a9eb23c792)

**Figure 8.** *Linear regression significance values*



## Final Analysis
Using the above analyses, we determined that mice treated with both Capomulin and Infubinol possessed a higher tumor volume than our other drug regmines of interest: Ramicane and Ceftamin. The linear regression revealed a significant positive association between tumor volume and mouse weight (*p* = 1.322e-07, *r* = 0.84) in mice treated with Capomulin.
