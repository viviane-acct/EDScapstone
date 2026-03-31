## Municipal Water Use Analysis Capstone Project 
<i>Relationship between population growth and residential per capita water use in 126 U.S. cities</i>

Author: Viviane Baji
<br>Environmental Data Science Certificate Program, Yale School of the Environment, Cohort 1</br>

Environmental Research Questions:

- How does population growth relate to water use? What kinds of cities are reducing their per capita water use?



Link to GitHub repository: [GitHub Repository](<https://github.com/viviane-acct/EDScapstone>)


This repo will contain project contents for the EDS capstone. Folders are:\
archive\
metadata\
outputs\
processed_data\
raw_data\
scripts

<b>Project Overview:</b>

Problem statement: Many US cities are growing rapidly which has water supply and infrastructure implications. 

Relevance: Each city has a number of policy tools available to manage the increase in water demand but implementation might vary.

Audience: US EPA Water- water research, infrastructure finance, municipal utility leaders

Dependent variable: Residential water use by city (logarithmic transformation)

### Project Approach

R libraries used:
#load libraries\
library(tidyr) #data organization\
library(ggplot2) #data visualization\
library(dplyr) #data cleaning\
library(GGally) #statistics\
library(janitor) #data cleaning\
library(lubridate) #dates\
library(stringr) #strings\
library(naniar) #missingness\
library(fixest) #fast estimation of linear models\

#more data viz libraries\
library(ggrepel)      #for smart label placement\
library(scales)       #for nice axis formatting\
library(sf)           #for maps \
library(ggrepel)      #repel on maps\

