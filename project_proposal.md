# Project Proposal

## Project Title
Predicting Annual Wine Production by Viticultural Region in Portugal

## Project Category
Tabular data / regression

## Team Members
- Nº 27916 | Andrea Dombe
- Nº 27916 | Dandara França
- Nº 26298 | Fernanda Chácara

## Problem Statement
This project investigates how to predict annual wine production for Portuguese viticultural regions using historical official statistics from the Instituto da Vinha e do Vinho (IVV).

Wine production is an interesting problem because it is an important agricultural and economic indicator, and it varies across regions and campaigns due to regional characteristics and changing production conditions.

## Challenges
The main challenge is the temporal structure of the data, since production changes from one campaign to another and the model must be evaluated without using information from future years.

Another challenge is that the data are aggregated by region, which limits the number of predictors directly available for modeling and may restrict model complexity.

## Dataset
The main dataset will be the IVV table **“Evolução da Produção Total por Região Vitivinícola”**, available at:
[https://www.ivv.gov.pt/np4/163.html](https://www.ivv.gov.pt/np4/163.html)

This dataset contains annual wine production values by viticultural region in hectoliters.

The data will be collected directly from the IVV statistics portal, which is the official public source for these records in Portugal.

If data integration is straightforward, the project may also use the IVV series **“Evolução da Área Total de Vinha - Portugal”** as an additional explanatory variable:
[https://www.ivv.gov.pt/np4/10586.html](https://www.ivv.gov.pt/np4/10586.html)

## Method or Algorithm
The proposed baseline method is **Linear Regression**, using year and viticultural region as the initial predictors.

If the dataset structure supports a slightly richer model without making the workflow too complex, vineyard area may be added as an extra feature, and a **Random Forest Regressor** may be tested as a comparison model.

## Evaluation
The results will be evaluated with standard regression metrics:
- MAE
- RMSE
- R²

The analysis will compare model performance across regions and campaigns.

The train/validation/test organization will respect chronological order so that evaluation reflects a realistic forecasting setting.
