# Temperature-Driven Demand and Grid Stabilization Risk Analysis  
### Switzerland (2020–2024)

## Project Description

This project analyzes how temperature variations relate to electricity demand,
grid stabilization activity, and associated economic risk in the Swiss electricity system.

Using daily data from 2020–2024, the analysis:

- Examines the temperature–demand relationship  
- Identifies nonlinear stabilization cost escalation  
- Defines a critical load threshold (≥ 2,100 MW)  
- Develops predictive models for demand sensitivity and critical-load probability  
- Simulates an operational scenario under extreme cold conditions (−7°C)

## Folder Structure

Project root directory:
```r
.
├── report.Rmd
├── README.md
├── styles.css
└── data/
  ├── Daily_Energy_Consumption2.rds
  └── daily_mean_temp.rds
```

- **report.Rmd** – Main analysis document (R Markdown report)  
- **styles.css** – Custom styling used in the rendered HTML output  
- **data/** – Contains input datasets in RDS format  


## Required R Packages

The following R packages are required to run the analysis:

```r
library(dplyr)
library(tidyr)
library(ggplot2)
library(lubridate)
library(forecast)
library(plotly)
library(knitr)
library(kableExtra)
```

To install missing packages:
```r
install.packages(c(
  "dplyr","tidyr","ggplot2",
  "lubridate","forecast",
  "plotly","knitr","kableExtra"
))
```

## Data Loading
All file paths are relative to the project root directory.

Datasets are loaded as follows:
```r
energy_data <- readRDS("./data/Daily_Energy_Consumption2.rds")
temp_data   <- readRDS("./data/daily_mean_temp.rds")

```
Ensure that the working directory is set to the project root
before running report.Rmd.

## How to Run

1. Open report.Rmd in RStudio

2. Set working directory to the project root

3. Click **Knit** to render the report

4. The analysis will automatically generate all figures and model outputs

## Methodological Overview

The project includes:

- Exploratory data analysis (EDA)

- Linear regression modeling (temperature–demand sensitivity)

- Logistic regression modeling (critical-load probability)

- Residual diagnostics

- Scenario-based risk simulation

## Author

Jihyeon Choung

MSc Applied Information & Data Science

Switzerland