
# Spatio-Temporal Analysis of Asylum Seekers Flow Across the Southern US Border

This project conducts a spatio-temporal analysis of border encounters at the U.S. southwest land border from 2000 to 2022. The dataset is sourced from the U.S. Customs and Border Protection (CBP) and includes monthly data on encounters for each border sector.

## Project Overview

### Data Acquisition
Collected monthly border encounter data from the CBP for all sectors of the southwest border, including Big Bend, Del Rio, El Paso, Laredo, and Rio Grande Valley.

### Spatio-Temporal Regression Model

#### Architecture & Performance
A spatio-temporal regression model was employed using Ridge regression, which incorporated features such as time (months) and spatial information (border sectors). The model demonstrated strong predictive power with the following performance metrics:

- **MSE**: 8,234,559.27
- **R²**: 0.826

### ConvLSTM Regression Model

#### Architecture & Performance
The ConvLSTM model, designed to capture both spatial and temporal dependencies in the data, was less effective than Ridge regression. Its performance metrics were as follows:

- **MSE (Unscaled)**: 25,527,465.39
- **R² (Unscaled)**: 0.445

### Comparison of Ridge Regression and ConvLSTM
In this analysis, Ridge regression clearly outperformed the ConvLSTM model. The Ridge model achieved a much lower MSE and a higher R² score, indicating better overall predictive performance.

### Policy Analysis

#### Title 42
A public health order that allowed border agents to expel migrants quickly during the COVID-19 pandemic. The DiD analysis showed that Title 42 had a negative impact on border encounters, though the effect was not statistically significant.

#### Remain in Mexico (Migrant Protection Protocols)
This policy required asylum seekers to remain in Mexico while their U.S. asylum cases were processed. Initially, this policy led to an increase in border encounters, but its impact declined over time.

### Difference-in-Differences (DiD) Analysis
A DiD analysis was conducted to evaluate the causal effects of the Title 42 and Remain in Mexico policies on border encounters. The analysis showed that both policies had a notable effect, with Title 42 reducing the number of encounters, although this effect was not statistically significant.

## Final Conclusions

1. **Ridge Regression** outperformed the ConvLSTM model in terms of predictive accuracy for forecasting asylum seeker flows across the southern U.S. border.
2. The **Difference-in-Differences analysis** provided insights into the impact of U.S. border policies, showing mixed effects from Title 42 and Remain in Mexico.
3. The analysis demonstrated the utility of spatio-temporal modeling for understanding the dynamics of migration flows over time.

