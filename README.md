# H1B Visa Petitions: A Comparative Analysis of Pre and Post Pandemic
![H1B image](https://github.com/itsritzz/H1-B_visa_petetions/blob/main/images/H1-B%20image.jpeg)

### Introduction
The H1B visa is a type of temporary work visa that allows highly skilled foreign workers to work in the United States. It is typically sponsored by a U.S. employer who is willing to offer the foreign worker a job and pay them a prevailing wage for their occupation. It is valid for up to three years and can be extended for an additional three years. To apply for an H1B visa, post an initial Labor Condition Application process approval, the employer can file an H1B visa petition with U.S. Citizenship and Immigration Services (USCIS). If the petition is approved, the foreign worker can then apply for an H1B visa at a U.S. embassy or consulate in their home country. 

## Data Sources
The data used in the project is Foreign Labor Certification (FLC) data - The FLC program provides data on the employment of foreign workers in the US, including H-1B visa holders. We used H1B data for the years 2017 to 2022. The data includes various attributes such as case status, received date, decision date, visa class, job title, employer details, wage information, and more.You can access this data on the Department of Labor (DOL) website [here](https://www.foreignlaborcert.doleta.gov/performancedata.cfm)

### Problem Statement
The impact of Covid-19 on the job market and global economy has led to a dearth of knowledge among H1B visa aspirants such as graduate students, mid-career professionals regarding factors such as approval rate, wage, etc which could be high for certain job titles, wage levels, industries, etc. As a result, many individuals are unsure on how to take their career forward. Therefore, the aim of this project is to provide accurate information on which factors have been majorly affected due to Covid-19 by utilizing data visualization, descriptive and inferential statistical methods. From the inferences, comparative trends in critical impact factors will be declared. This shall bridge the knowledge gap and provide clarity to our target audience by bridging their knowledge gap and answering the big question i.e., whether Covid-19 had an impact on the H-1B petition process.

## Required Packages
Before running the code, ensure you have the necessary R packages installed. You can install them using the following code:

```R
#install.packages("dplyr")
#install.packages("tibble")
#install.packages("ggplot2")
#install.packages("hrbrthemes")
library(dplyr)
library(tibble)
library(ggplot2)
library(hrbrthemes)
library(ExcelFunctionsR)
```
## Data Loading

The code reads the H1B visa data for each year from 2017 to 2022 into separate data frames. Data columns of interest are selected, including case status, dates, visa class, job details, employer information, wage, and more.

## Data Preprocessing

Calculates the time taken for case processing by computing the difference between the decision date and received date.
Extracts the first two digits of the SOC code.
Filters out missing case status records.
Filters records to consider only H-1B visa class applications.
Appends the respective year to each dataset.

## Industry Analysis

Conducts an analysis of the industry based on SOC codes.
Loads the SOC code lookup table.
Matches SOC codes to their corresponding industries.
Filters datasets based on selected SOC codes for the analysis.

## State Analysis

Filters datasets based on employer states in the United States.
Separates data into certified and denied cases.
## Visualization

Generates heatmaps to visualize the frequency of applications by state for each year.
Creates bar charts to show the top 10 states with the highest number of H1B filings.
Plots industry-wise statistics, including the average wage and number of applications.
Displays scatter plots of average wage versus the number of applications for different industries.
Creates stacked bar charts for case status analysis by visa class and full-time position.
## Log Transformation

Calculates the logarithm with base 1.5 of the time taken for case processing.
Conducts a histogram analysis to understand the distribution.
## Wage Analysis

Analyzes wage data through histograms and box plots.
Performs statistical tests to compare the pre-COVID-19 and post-COVID-19 time taken.
## Conclusion

This project provides insights into H1B visa application trends, industry-wise distribution, case status, and wage analysis. The visualizations and data transformations help in understanding various aspects of the H1B visa process.

For a detailed analysis, you can refer to the [R files](https://github.com/itsritzz/H1-B_visa_petetions/tree/07b3e313b64cd13ad3b9aba696a116c4bd416460/R%20files) in this repository.
