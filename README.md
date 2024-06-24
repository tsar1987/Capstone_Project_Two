# Residential House Prices Prediction in Wake County, North Carolina with Machine Learning
## Introduction
1. The residential house market in Wake County, NC is highly competitive, with properties receiving an average of 5 offers and selling in just 37 days. 
2. Use historical sale data, property features and economic indicators.
3. Aim to provide accurate and actionable pricing and remodeling recommendations to buyers and sellers.
## Audience
1. House buyers, sellers and real estate agents in Wake County, NC 
2. Example question1: What is a reasonable price for the property I am interested in buying? 
3. Example question2: What is the optimal listing price for my property? 
4. Example question3: What are the key factors influencing the predicted prices?
## Data
1. Historical Sale Data
one csv file from Wake County, North Carolina real estate website
441328 rows and 87 columns, including information about owner, mail address, real estate id, street, sale, deed, heated area, utility, exterior wall, design style, city etc.
https://www.wake.gov/departments-government/tax-administration/data-files-statistics-and-reports/real-estate-property-data-files
2. Economic Indicators
1 csv file from U.S. BUREAU OF LABOR STATISTICS
51 rows and 3 columns, including population density and unemployment data from 1973 to 2023.
https://data.bls.gov/timeseries/LASST370000000000003?amp%253bdata_tool=XGtable&output_view=data&include_graphs=true
## Exploratory data analysis (EDA)

Top 4 city in dataset: Raleigh, Cary, Apex, Wake Forest.

![image](https://github.com/tsar1987/Capstone_Project_Two/assets/125304961/f546e755-3f40-44ea-a35d-e75450ee4a20)

Top 4 sale year in dataset: 2021, 2020, 2022, 2019. Obvious dip around 2018-2012 because of economic crisis.

![image](https://github.com/tsar1987/Capstone_Project_Two/assets/125304961/43c14eb2-20aa-4e67-bce3-eaf2708c4b14)

House price for each city with outliers.

![image](https://github.com/tsar1987/Capstone_Project_Two/assets/125304961/c7ead80c-93c0-41ac-be52-53bff7cf04bb)

House price for each city without outliers. Remove outliers larger than 75 percentile +1.5*IQR

![image](https://github.com/tsar1987/Capstone_Project_Two/assets/125304961/7c4cf24d-f005-4c82-a0fe-71aedd6e625a)
## Data Training and Modeling
![image](https://github.com/tsar1987/Capstone_Project_Two/assets/125304961/119a1555-e96b-4d59-8d90-f020feac5afa)
![image](https://github.com/tsar1987/Capstone_Project_Two/assets/125304961/5380ded0-8123-4b73-af9c-76538c3c3cb3)
## Conclusion
![image](https://github.com/tsar1987/Capstone_Project_Two/assets/125304961/7df947e3-5425-49dd-9a37-395e54df4fba)

Gradient boost regression model performs best in all four models I tested. The model performs very well for house price less than 3 million, for house price higher than 3 million, the predictive ability is weak, which means the model still not very good at handling high value outliers.
## Future Work
1. Collect more recent data into the training set could be beneficial, as it may capture evolving trends and market dynamics that impact house prices. 
2. Explore feature engineering techniques or introducing new relevant features, such as neighborhood developments, or seasonality factors, could improve the model's ability to adapt to changing conditions. 
3. Fine-tuning more hyperparameters of the Gradient Boosting Regressor or experimenting with alternative algorithms might also be considered to optimize predictive accuracy. 
4. Combine predictions from multiple models may provide a more robust and accurate prediction for house sales.














