# Capstone Project: Predicting Life Expectancy for Developing Countries

## Overview

This model predicts life expectancy for developing countries using machine learning techniques. By analysing historical data from authoritative sources, such as the World Health Organization (WHO), the model seeks to provide valuable insights for policymakers, researchers, and social organisations. These insights could help develop and enhance healthcare strategies, improve resource allocation, and drive targeted interventions to improve public health outcomes in these regions.

**Project Goals**

- Create data driven solution to predict life expectancy in developing countries.
- Identify key factors that influence life expectancy, such as healthcare, education, and economic development.
- Provide insights to enable regions to increase life expectancy by targeted healthcare and education improvements.

## Data

The project uses public data from authoritative sources, _The World Health Organization_, _World Bank_, and _Our World in Data_. The dataset provides annual information about health and economic conditions for 179 countries, 142 of which are developing, between 2000 and 2015. A detailed description of the data can be found in the [data_sheet](data_sheet.md). 

Key areas covered in the data include:
- Health: Life expectancy, adult and infant mortality, immunisation and disease rates.
- Economy: GDP per capita, Development status.

## Model
**How the model works**

To make accurate predictions, we used a machine learning model called _XGBoost_. XGBoost is a well established model which is highly optimised for structured datasets like this one. The model looks at the historical data from many developing countries and tries to understand which factors are most important in predicting life expectancy. It then uses this knowledge to make predictions for scenarios that were not part of the original data. XGBoost contains a number of specific implementation parameters and we optimised these to find the best model. Further details can be found in [model_card](model_card.md)

**Performance Metrics**

To test how well the model works, we divided the data into two parts: one part, comprising 80% of the dataset, was used to train the model, and the remainder was used to test it. The model was able to predict life expectancy on the test set with a standard deviation of about 0.6 years. This means that if the model predicts that a country will have a life expectancy of 70 years, the actual life expectancy is very likely to lie between 69 years or 71 years. This small difference shows that the model is accurate, but it's not perfect.

**Generalisability**

The model performance was assessed using data from the that it hadn’t seen before to ensure it did not overfit to the training data. An analysis of the most important features influencing performance showed similar results from both the training and test set again confirming that it was reliable and can be used to predict life expectancy for other scenarios not in the dataset. 

## Conclusion
This project shows how machine learning can help predict life expectancy in developing countries and provide valuable insights to improve healthcare strategies. The model helps us understand which factors—like healthcare, economy, and education—are most important for improving life expectancy.

**How Can This Help?**
By using the model’s predictions, governments and organizations can make better decisions about where to focus healthcare resources and policies. For example, if a country’s life expectancy is lower than expected, the model can suggest areas that need improvement, such as increasing healthcare spending or focusing on education.

**Future Improvements**
- The model can be updated with more recent data to improve its predictions.
- Future work could explore adding gender to understand the differences and drive more specific healthcare strategies.
- The model could be used to make predictions for specific regions or communities within countries to provide more detailed guidance.
