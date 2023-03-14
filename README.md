# World Happiness Report

Advanced Projects in Machine Learning, Spring 2023

Aim: Predict happiness level for country *i* given country-level data

### Data:

Description of input data:
![frequency of happiness answers](https://github.com/lprockop/WorldHappinessReport/blob/main/hist.png?raw=true)
![frequency of happiness answers](https://github.com/lprockop/WorldHappinessReport/blob/main/simplevars.png?raw=true)

#### Primary datasource from WHR:

##### Columns: 
'Happiness',
'Country or region',
'GDP per capita',
'Social support',
'Healthy life expectancy',
'Freedom to make life choices',
'Generosity',
'Perceptions of corruption',
'name',
'region',
'sub-region',
'Terrorist_attacks',
'country_name_x',
'population_x',
'population_below_poverty_line_x',
'hdi_x',
'life_expectancy_x',
'expected_years_of_schooling_x',
'mean_years_of_schooling_x', 
'gni_x',
'country_name_y',
'population_y',
'population_below_poverty_line_y',
'hdi_y',
'life_expectancy_y',
'expected_years_of_schooling_y',
'mean_years_of_schooling_y',
'gni_y'
 
 Bivariate distribution of key features: 
 ![bivariate dist](https://github.com/lprockop/WorldHappinessReport/blob/main/bivar.png?raw=true)

 #### Secondary datasource: 'newcountryvars.csv'
 
 ##### Columns: 
 'country_name', 
 'population', 
 'population_below_poverty_line', 
 'hdi', 
 'life_expectancy', 
 'expected_years_of_schooling', 
 'mean_years_of_schooling', 
 'gni'


### Outcomes: 

First, I submitted a Gradient Boosting Classifier, Random Forest Classifier, and KNN Classifier. These models didn't perform particularly well and appeared to be overfit to the training data. The random forest had accuracy 0.441176 and f1 below 0.4 for both models. My team's advice was to test different architectures, including suggested a Bagging Classifier and SVC. They also suggested changing the hyper-parameters. 

After hyper-parameter tuning, I submitted a Bagging Classifier, SVC, and a few other Gradient Boosting Classifiers with different hyper parameters. The final models are shown below.

Only two models had accuracy above 0.5. Neither had f1 scores above 0.5. The two best models were gradient boosted classifier and SVM. 

Overall, the best performing model was a gradient boosted classifier with hyper parameters: {'learning_rate': 1, 'n_estimators': 101}. The accuracy was 0.529412 for this model and f1 score was 0.496121. All of the models and their comparative metrics are shown below.
