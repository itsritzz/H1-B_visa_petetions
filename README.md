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

## Result
After our analysis, we found that despite COVID-19's impact on the labour market and the global economy, the H-1B petition filing process has not been significantly changed. However, because of the global uncertainty caused by the pandemic, applicants filing for H-1B visas are less informed about the current scenario of the trends. Based on the data visualization, the stacked bar chart in Figure 2 shows a rise in the proportion of certified cases and a fall in the proportion of denied cases following the pandemic. The median of prevailing wages has increased after the pandemic, according to the box plot in Figure 3. In the pre-covid 19 scenarios compared to the post-covid 19 scenario, Figure 4 shows a significant increase in visa petitions filed for the computer and mathematical, management, life, physical and social science, and architecture industries while a decrease in petitions filed for the business and financial operations, art design, entertainment, sports, and media industries. Figure 5 indicates that the processing time log for petitions submitted increased marginally from 4-5 days prior to Covid to 5-6 days following Covid, proving that Covid did not significantly affect processing time.

Majorly California experienced an increase in H-1B petitions post-covid 19, while Texas and states on both coasts, including New Jersey, New York, and Washington, saw a minor decline in petitions filed compared to pre-covid 19 (Figure 6). According to the number of applicants, the average income is shown in Figure 7's scatter plot, with the legal, computer, and mathematics industries being the only pre- and post-covid 19 outliers.

Based on the heatmap presented, most petitions filed prior to the COVID-19 pandemic were concentrated in the eastern region. It is important to note, however, that this distribution may have shifted in response to the pandemic, as many individuals and businesses have relocated or altered their behaviour due to changing circumstances. Overall, this analysis has provided valuable insights towards solving the knowledge gap for our target audience.

For a detailed analysis, you can refer to the [R files](https://github.com/itsritzz/H1-B_visa_petetions/tree/07b3e313b64cd13ad3b9aba696a116c4bd416460/R%20files) in this repository.
