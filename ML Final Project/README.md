# Final Project - Modelling part

### Machine Learning Foundations with Python (90-803)

#### Spring 2023

#### Yilin Lyu

### Title

Analysis of COVID-19 infection and fatality in the United States from 2020-2023.

### Authors

Yilin Lyu (Andrew: yilinlyu | Andrew Email: yilinlyu@andrew.cmu.edu |Github: YLtryingcode)

--

### Disclaimer / Sensitive Content

The following data pertains to the COVID-19 pandemic and includes information related to mortality rates, confirmed cases, and hospitalization rates. Please be advised that this content may be sensitive and potentially triggering for individuals who have experienced personal loss, trauma, or grief related to the pandemic. I understand that COVID-19 has impacted countless lives in significant and profound ways, and I offer my sincerest condolences to those who have lost loved ones. If this topic is likely to cause distress or discomfort, I kindly advise that you avoid further reading. I encourage all readers to prioritize their mental and emotional well-being above all else.

--

### Project Description

COVID-19 impacted the world dramatically in the past couple of years. Although it seems like we are past the stage where we worry about the pandemic, COVID-19 will not be the last pandemic in our lifetime as we continue to. Therefore, understanding how personal behavior and medical resources impact the outcome of a pandemic is an important thing we can learn from this.

This project focuses on using machine learning models to study, analyze and predict COVID-19 outcomes. Our response to COVID-19 from the past years will chart the course of action for the coming years when it comes to the mutations of the same disease or infections that affect the human respiratory system.

The independent variable will include personal behavior, such as mask-wearing and vaccine acceptance, and medical resources such as healthcare expenditure. And the outcome variables will be the percentage of covid confirmed cases. The entire project focuses on using prediction models such as linear regression, polynomial regression, decision tree, and random forest. In addition to that, I also tried the classification model and XGBoost for better accuracy.

**Key Words** - Covid-19 Analysis, Covid-19 Infection Rate, Hospital Admission in US, Covid-19 related Death, vaccine, political leaning

**Questions** - Include your final questions here.

1. Predict the percentage of positive COVID-19 tests of in the U.S. based on individual life decision behaviors and medical behaviors.
   Target Variable: Percentage of positive COVID-19 tests

### Data Collection

- To run the data cleaning and visualiztaion notebook:
  https://drive.google.com/drive/folders/1klT5FxKs6_ovvNJwTMby9X3oBDsyHYBc?usp=sharing
  To run each model notebook please download the dataset from this link:
  https://drive.google.com/drive/folders/1EL22rVqw_alk3SbX_mjmm7ZWbtS9soRU?usp=share_link

Group, D. (no date) About Covidcast, Delphi Data . Available at: https://cmu-delphi.github.io/delphi-epidata/ (Accessed: May 2, 2023).

To use API:
One should first download ‘covidcast’ from prompt
Write the following code in a notebook cell:
-Import covidcast
from datetime import date
data = covidcast.signal("fb-survey", "smoothed_cli", date(2020, 5, 1), date(2020, 5, 7), "county")
This will offer data of cli from Facebook survey between 2020/05/01-2020/05/07
For more details, please see the “Data Cleaning & Visualization Final.ipynb”

### Conclusions and Discussions

-Overall, this project aimed to use machine learning models to study, analyze, and predict COVID-19 outcomes, specifically the percentage of confirmed cases, hospitalizations, and deaths caused by COVID-19. The project faced challenges due to the time-based nature of the data and the many factors that can impact the outcome variable beyond personal behavior and medical resources, including policy changes, vaccine availability, and different versions of the virus.

For predicting COVID-19 confirmed cases, the best model was a Random Forest Model, while clustering and confirmed death were the most important features for prediction. For hospitalization, the best prediction models involved fitting a polynomial regression model of degree 2 and adding 3 clusters made out of the features. And if turning the prediction to a classification question, KNN had the best accuracy but overall performed poorly. For COVID-related deaths, the best model was Gradient Boosting Regressor, but all models performed poorly due to the time-series nature of the data as all models tend to overfit the training data and fail to predict the trend in testing data.

Future work should focus on including more data, such as event data that has a significant impact on the overall society and using time series models. It would also be beneficial to add more features, such as age and medical conditions, to predict COVID-19 deaths. Additionally, future analysis could investigate if the features in the dataset predict how COVID-19 will spread later in the United States. Despite the challenges faced, machine learning remains a valuable tool for increasing the power of epidemiological and decision-making models within public health.

### Future Work

Since the data is time series data, in the future, I will do more careful to pick the “right” dataset
Since the models are predicted to be very bad in general, I will want to add more features into the dataset, such as age, gender, medical condition, etc.
Since I used the Delphi website, the data resources are all from different surveys, which are not highly trusted. So in the future, I want to get a more reliable dataset, such as the CDC dataset.

### Running the Project / Getting Started

The first part of this project is data collection, cleaning and visualiztaion. One should first download all the datasets from the following link:
https://drive.google.com/drive/folders/1klT5FxKs6_ovvNJwTMby9X3oBDsyHYBc?usp=sharing

After having all the datasets at one place, one should download the “Data Cleaning & Visualization Final.ipynb '' from GitHub and run the Jupiter notebook.

At the end of the Data Cleaning & Visualization Final.ipynb, the notebook will generate a csv called ‘covid_cleaned.csv’ for the data collection. This CSV file can also be found from this link: https://drive.google.com/drive/folders/1EL22rVqw_alk3SbX_mjmm7ZWbtS9soRU?usp=share_link

Covid_cleaned.csv file is needed to run all three notebooks for modeling.

### NOTE :

You might receive a warning for Kmeans depending on which version of Python you are running
The random forest tuning takes a very long time, you might have to let it run based on the processing time for your computer or convert it into a markup cell
Installation Required on Anaconda Prompt :
Pip install covidcast (Optional, if you want to uncomment and run the API call)
pip install XGBoost
