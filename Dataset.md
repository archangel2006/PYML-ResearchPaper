# Dataset

Life Expectancy (WHO) : https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who

---
# Dataset History 
(obtained from Kaggle)

- The Global Health Observatory (GHO) data repository under World Health Organization (WHO) keeps track of the health status as well as many other related factors for all countries.
- The datasets are made available to public for the purpose of health data analysis. The dataset related to life expectancy, health factors for 193 countries has been collected from the same WHO data repository website and its corresponding economic data was collected from United Nation website.
- Among all categories of health-related factors only those critical factors were chosen which are more representative. It has been observed that in the past 15 years , there has been a huge development in health sector resulting in improvement of human mortality rates especially in the developing nations in comparison to the past 30 years. 
- Therefore, in this project we have considered data from year 2000-2015 for 193 countries for further analysis. The individual data files have been merged together into a single dataset. On initial visual inspection of the data showed some missing values. As the datasets were from WHO, we found no evident errors. 
- Missing data was handled in R software by using Missmap command. The result indicated that most of the missing data was for population, Hepatitis B and GDP. The missing data were from less known countries like Vanuatu, Tonga, Togo,Cabo Verde etc. 
- Finding all data for these countries was difficult and hence, it was decided that we exclude these countries from the final model dataset. The final merged file(final dataset) consists of 22 Columns and 2938 rows which meant 20 predicting variables. 
- All predicting variables was then divided into several broad categories:​Immunization related factors, Mortality factors, Economical factors and Social factors.

# Dataset Columns

1. Country
2. Year : Year
3. Status : Developed or Developing status
4. Life expectancy : Life Expectancy in age
5. Adult Mortality : Adult Mortality Rates of both sexes (probability of dying between 15 and 60 years per 1000 population)
6. infant deaths : Number of Infant Deaths per 1000 population
7. Alcohol : Alcohol, recorded per capita (15+) consumption (in litres of pure alcohol)
8. percentage expenditure : Expenditure on health as a percentage of Gross Domestic Product per capita(%)
9. Hepatitis B : Hepatitis B (HepB) immunization coverage among 1-year-olds (%)
10. Measles : Measles - number of reported cases per 1000 population
11. BMI : Average Body Mass Index of entire population
12. under-five deaths : Number of under-five deaths per 1000 population
13. Polio : Polio (Pol3) immunization coverage among 1-year-olds (%)
14. Total expenditure : General government expenditure on health as a percentage of total government expenditure (%)
15. Diphtheria : Diphtheria tetanus toxoid and pertussis (DTP3) immunization coverage among 1-year-olds (%)
16. HIV/AIDS : Deaths per 1 000 live births HIV/AIDS (0-4 years)
17. GDP : Gross Domestic Product per capita (in USD)
18. Population : Population of the country
19. thinness 1-19 years : Prevalence of thinness among children and adolescents for Age 10 to 19 (% )
20. thinness 5-9 years : Prevalence of thinness among children for Age 5 to 9(%)
21. Income composition of resources : Human Development Index in terms of income composition of resources (index ranging from 0 to 1)
22. Schooling : Number of years of Schooling(years)
