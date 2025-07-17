# Buying Friends? 
# Modelling Pro-Russian Voting Behaviour in the UNGA

## Project Overview

**Description**: Final Iron Hack Machine Learning Project (Data Science End to End)

**Team**: Maria

**Topic**: Country Voting Alignment with Russia in the United Nations General Assembly (UNGA)

**Title**: Buying Friends?

**Question**: What drives other countries to support Russia by voting in line with its interests in the United Nations General Assembly? (goal is identifying features of countries that support Russia in resolutions)

**Target Variable**: "Pro-Russian Voting Index" calculated based on 35 selected UNGA votes relevant for Russian foreign policiy (Ukraine, Georgia)

**Features** based individual UN members: Russian Official Development Assistance, Bilateral Investment Treaty with Russia, Export and Import Partner Share, Regime Type, Distance between capitals, Comecon membership, Defence Cooperation Agreement, GDP per capita, Regional Organisation member with Russia (mean values are based on target variable 2008-2023) 

**Various Data Sources**: 
- United Nations Digital Library | Voting Data. https://digitallibrary.un.org/search?ln=en&cc=Voting+Data (target variable)
- OECD: QWIDS - Query Wizard for International Development Statistics. https://stats.oecd.org/qwids/
- WITS: Russian Federation Trade Balance, Exports, Imports by Country 2021 | WITS Data. https://wits.worldbank.org/CountryProfile/en/Country/RUS/Year/2021/TradeFlow/EXPIMP/Partner/by-country
- UNCTAD: Russian Federation | International Investment Agreements Navigator | UNCTAD Investment Policy Hub. https://investmentpolicy.unctad.org/international-investment-agreements/countries/175/russian-federation
- Boix, C., Miller, M. & Rosato, S. (2022) Boix-Miller-Rosato Dichotomous Coding of Democracy, 1800-2020. Harvard Dataverse, V1. https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/FENWWR
- Kinne, B. J. (2018) Replication Data for: Defense Cooperation Agreements and the Emergence of a Global Security Network. Harvard Dataverse, V1. https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/5XKNPS
- Oxford University Press: COMECON. https://www.oxfordreference.com/display/10.1093/oi/authority.20110803095626480
- The World Bank: World Development Indicators | DataBank. https://databank.worldbank.org/source/world-development-indicators
- GeoDist Database: http://www.cepii.fr/distance/dist_cepii.dta.
- United Nations: Member States. https://www.un.org/en/about-us/member-states#gotoV

## Project Presentation

Link: https://www.canva.com/design/DAGg-H6A3s4/bXEk58NHn34EchdTY5hEJQ/edit 


**Buying Friends? - Modelling Pro-Russian Voting Behaviour in the UNGA**

This project aims to model and analyse the factors that drive countries to support Russia by voting in line with its interests in the United Nations General Assembly (UNGA). The primary hypothesis is that economic ties and dependencies on Russia are the strongest predictors of voting alignment.

Research Question: What drives other countries to support Russia by voting in line with its interests in the UNGA?

Hypothesis: A country's economic ties and dependencies on Russia are the strongest predictors of its voting alignment with Russia in the UNGA.


**Dataset**

Size: 192 rows (UN member states) × 12 columns

Timeframe: 2008-2023

Sources: Self-constructed from various sources (UN voting data, OECD, UNCTAD, etc.)

Target Variable: Pro-Russian Voting Index (continuous values between 0 and 1)

Based on 35 key UNGA resolutions (Ukraine, Georgia, etc.) from 2008-2023

Coding: Support = 1, Against = 0, Abstention/Absence = 0.5

Index per country calculated as the arithmetic mean

Features

Economic Factors: Mean Russian Aid Amount per Year ($MM), Bilateral Investment Treaty with Russia (0/1), Export and Import Partner Share, GDP per capita ($)

Other Factors: Regime Type (democratic/authoritarian), Distance to Moscow (km), Comecon Membership (0/1), Defence Cooperation Agreement with Russia (0/1), Membership in Regional Organisations with Russia (0/1)


**Data Processing & Feature Engineering**

Exploratory Data Analysis:

Target variable (Pro-Russian Voting Index) is not normally distributed

Applied Quantile Transformer for normalization to achieve a more normal distribution

Normalisation of features (GDP per capita, distance to Moscow) for distance-based models due to large differences in values

Feature Selection:

Low correlation with target (< 0.1): Dropped Bilateral Investment Treaty, Comecon Membership, Import Partner Share

High correlation among features:Import Partner Share with Export Partner Share but Import already dropped 

Feature Engineering:

Normalisation of features to improve model performance in distance-based models


**Machine Learning Models & Performance**

KNN | normal R² = 0.50 | Cross-Validation R² = 0.42

Linear Regression | normal R² = 0.32 | Cross-Validation R² = 0.28

Decision Tree | normal R² = 0.65 | Cross-Validation R² = 0.36

Random Forest | normal R² = 0.61 | Cross-Validation R² = 0.56 

Ada Boost | normal R² = 0.54 | Cross-Validation R² = 0.53

Gradient Boost | normal R² = 0.46 | Cross-Validation R² = 0.51

Best Model: Random Forest (R² = 0.56)

Challenges: Performance drop after cross-validation due to small dataset size and high feature variability

Trade-Offs: Predictions can be back-transformed, but coefficients are not interpretable in the original scale

Cross-validation insight: Random state 42 was found to perform better than the average across multiple train/test splits


**Key Findings**

Top Predictors of Pro-Russian Voting:

Russian Aid: Countries receiving more Russian development assistance tend to align with Russia in voting (35.39% importance in the Random Forest model)

Distance to Moscow: Russia gains more voting support from geographically distant countries (20.60% importance)

Regime Type: Authoritarian countries have a higher voting alignment with Russia than democracies (20.08% importance)

GDP per Capita: Lower GDP per capita is associated with higher Pro-Russian voting (18.44% importance)

Rejected Predictors:

Import/Export Partner Share and Bilateral Investment Treaties were not significant predictors

Defence Cooperation Agreements and Membership in Organisations with Russia showed minimal impact

Evidence for Initial Hypothesis:

Economic dependencies, particularly Russian aid, are the strongest predictors of Pro-Russian voting alignment in the UNGA

Economic ties such as import/export partnerships and treaties were not as relevant as direct aid and GDP


**Limitations & Future Work**

Dataset Size: The relatively small dataset may limit generalisability

Missing Features: Additional variables could improve predictive power (e.g., military alliances, historical ties, internal political stability)

Explaining vs. Predicting

The focus of this project is explaining the key features that influence Pro-Russian voting rather than making future predictions.

Since there are no "new" countries joining the UN, the model has limited practical application for predicting voting behaviour beyond changes in country characteristics.

Alternative Models:

More advanced models could be explored for robustness

Time-series analysis could track trends in Pro-Russian voting over time


**Conclusion**

The analysis confirms that economic dependencies on Russia, especially through aid and lower economic standing (GDP per capita), significantly influence voting alignment with Russia in the UNGA. While the Random Forest model performed best, further refinements in feature selection and theoretical research could enhance explanatory power.

Author: Maria
Project: Data Science End-to-End 
Case StudyTimeframe: 2008-2023
