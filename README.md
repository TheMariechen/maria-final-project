# maria-final-project

**Description**: Final Iron Hack Machine Learning Project (Data Science End to End)

**Team**: Maria

**Topic**: Country Voting Alignment with Russia in the United Nations General Assembly (UNGA) 

**Title**: need to find short and catchy title for topic

**Question**: What drives other countries to support Russia by voting in line with its interests in the United Nations General Assembly? (goal is identifying features of countries that support Russia in resolutions)

**Target Variable**: "Pro-Russian Voting Index" calculated based on 36 selected UNGA votes relevant for Russian foreign policiy (Ukraine, Georgia etc.) 

**Features** based individual UN members: Russian Official Development Assistance, Bilateral Investment Treaty with Russia, Export and Import Partner Share, Regime Type, Distance between capitals, Comecon membership, Defence Cooperation Agreement, GDP per capita, Regional Organisation member with Russia 

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

**Plan**: 
- Read: "How to avoid machine learning pitfalls: a guide for academic researchers"
- Descriptive Statistics
- Visualization Board in Tableau 
- Handling Outliers etc.
- Feature Engineering: Normalization of values very much required!
- Feature Selection: Make sure to include only most relevant features in model
- Apply Machine Learning (regression) in depth: try all models to find best one
- In addition to regression, try out classification (support: yes/no)
- Use hyperparameter tuning, cross-validation etc.! 
- If time: webscrape additional sources to enrich number of features and/ or webscrape target variable again with additional votes 
- If time: more advanced models that we did not cover yet time-series etc. (split target variable into different years)
- Create Presentation (reserve whole last day!)
