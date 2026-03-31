## Municipal Water Use Analysis Capstone Project 
<i>Relationship between population growth and residential per capita water use in 126 U.S. cities</i>

Author: Viviane Baji
<br>Environmental Data Science Certificate Program, Yale School of the Environment, Cohort 1</br>

Environmental Research Questions:

- How does population growth relate to water use? What kinds of cities are reducing their per capita water use?



Link to GitHub repository: [GitHub Repository](<https://github.com/viviane-acct/EDScapstone>)


This repo contains project contents for the EDS capstone. Folders are:\
archive\
metadata\
outputs\
processed_data\
raw_data\
scripts- see notebook here for full capstone project

### Project Overview

<b>Problem statement:</b> Many US cities are growing rapidly which has water supply and infrastructure implications. \
<b>Relevance: </b> Each city has a number of policy tools available to manage the increase in water demand but implementation might vary.\
<b>Audience: </b> US EPA Water- water research, infrastructure finance, municipal utility leaders


<b>Project Feasibility:</b> 
- Minimum dataset: Municipal water use dataset
- Risks: Not all major US cities are included in the dataset. Residential/Commercial breakdown is not available for all cities.
- Feasibility statement: The project is feasible with accessible, free datasets; some preprocessing is needed, but outcome and predictors exist.

<b>Data Stewardship:</b>
- No Personally Identifying Information (PII). All public datasets.
- Versioning with GitHub.
- Citation for datasets:
Chinnasamy, C. V., Arabi, M., Sharvelle, S., Warziniack, T., Furth, C. D., & Dozier, A. (2021). Characterization of municipal water uses in the contiguous United States. Water Resources Research, 57, e2020WR028627. https://doi.org/10.1029/2020WR028627


I set out to understand what drives municipal water use trends. Using a municipal water use dataset for 126 cities from 2005-2017, I was able to explore water use and discover links between population growth and water use using R libraries and analytical approaches. I found that per capita water use is lower in growing U.S. cities while cities that are not growing use more water overall but have reduced it over time. There could be more conservation potential in older cities, whereas newer ones are more efficient. This has implications for understanding how water resources will be impacted by growth.


### Project Approach and R Libraries Used

Data Cleaning:
- library(tidyr) #data organization
- library(dplyr) #data cleaning
- library(janitor) #data cleaning
- library(lubridate) #dates
- library(stringr) #strings
- library(naniar) #missingness
  
Data Exploration/Visualization
- library(ggplot2) #data visualization

Mapping
- library(ggrepel)      #for smart label placement
- library(scales)       #for nice axis formatting
- library(sf)           #for maps 
- library(ggrepel)      #repel on maps

#### Analysis Variables & Hypotheses
<b>Dependent variable:</b> Residential water use by city (logarithmic transformation)\
Predictors:\
•	whether a city grew by 100,000 people in any 5-year period between 2010 and 2017 (1/0).\
•	climate region (categorical)\
Equation sketch:\
feols(log(res_billed_gallons) ~ city_big_growth_percent | us_census_id,   \   
               data = muni_water_clean_analysis_rate)\
               
Libraries
- library(fixest) #fast estimation of linear models
- library(GGally) #statistics

