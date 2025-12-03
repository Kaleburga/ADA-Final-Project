NHANES Diabetes & Insurance Analysis

#Project Description

This repository contains the R code and NHANES 2021–2023 survey data used to examine the association between health insurance status and poor glycemic control among U.S. adults with diagnosed diabetes. The analysis focuses on understanding whether insurance coverage is associated with hemoglobin A1c (HbA1c) levels while accounting for demographic and clinical factors. The project also explores effect modification by age and performs sensitivity analyses.

#Files Included
    •	DEMO_L.XPT, DIQ_L.XPT, HIQ_L.XPT, BMX_L.XPT, GHB_L.XPT: NHANES 2021–2023 datasets (demographics, diabetes status, insurance, BMI, HbA1c)
    •	analysis_code.Rmd: R Markdown code for cleaning, merging, visualizing, and analyzing the data
    •	README.md: This file

#What the Code Does
  1.Data Import & Cleaning
      •	Reads NHANES datasets and selects relevant variables
      •	Merges datasets by participant ID
      •	Applies exclusions (non-diabetic, pregnant, missing outcome or covariates)
      •	Recodes and categorizes variables for analysis
  
  2.Descriptive Analysis
      •	Generates a flowchart showing participant inclusion/exclusion
      •	Creates Table 1 summarizing demographics, socioeconomic, and clinical variables by insurance status
      •	Visualizes insurance status distribution by poor glycemic control
  
  3.Survey Design & Modeling
      •	Implements survey-weighted logistic regression models to examine associations between insurance status and poor glycemic control
      •	Adjusts for potential confounders: age, sex, BMI, race, education
      •	Assesses effect modification by age group (<60 vs ≥60) using interaction terms and stratified models
      •	Checks model assumptions: linearity, multicollinearity (VIF), influential observations (Cook’s distance)
      •	Performs sensitivity analyses with HbA1c ≥7.5%

#How to Run the Code
   1.	Download or clone this repository to your computer
   2.	Ensure the NHANES .XPT files are in the same folder as the R Markdown file
   3.	Open analysis_code.Rmd in RStudio
   4.	Install required packages if necessary:
        “pacman::p_load(odds.n.ends, DiagrammeR, DiagrammeRsvg, blorr, glue, haven, survey, ggplot2, lmtest, car, rsvg, broom, dplyr, tidyverse, readr, jtools, table1, rvg, officer, htmlwidgets, webshot2)”
   5.	Run the R Markdown file to reproduce the tables, figures, and models

#Author
  	Name: Kaleb Urga
    Course: Advanced Data Analysis
