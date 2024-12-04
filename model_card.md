# Model Card
The model predicts the life expectancy based on a number of other key health indicators. The World Health Organization (WHO) defines life expectancy as the average number of years a person can expect to live in a specific area, based on current mortality rates.

The model was trained on a dataset available in Kaggle: [Life Expectancy (WHO) Fixed](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated). This was based on primary data sources from _WHO_, _World Bank_, and _Our World in Data_. More details on the data set can be found in [Data_Sheet.md](Data_Sheet.md).

## Overview

#### Developer
This model was constructed in a private capacity.

#### Intended Usage
This model is intended for research purposes and should not be used for policymaking without further investigation into accuracy and potential biases.

## Model Description

**Input:** 
The inputs are a number of different health and population indicators. These are described in more detail in [Data_Sheet.md](Data_Sheet.md).

**Output:**
The model output is the prediction for the life expectancy.

**Model Architecture:** 
The model uses version 2.1.1 of the [XGBoost](https://xgboost.readthedocs.io/en/stable/get_started.html) library with the following parameters:

- Learning Parameter, eta: 0.01
- Maximum depth of the tree, max_depth: 8

## Performance
The model was assessed using the following metrics:

- Mean squared error
- Mean absolute error
- Mean absolute percentage error
- Maximum Error, $`\max_i |X^{(i)}_{predict} - X^{(i)}_{actual}|`$
- $`R^2`$ Score, [Coefficient of determination](https://en.wikipedia.org/wiki/Coefficient_of_determination) 

Calibrating the model using 20\% of the data sample gave the following performance:

- Mean squared error: 0.393
- Mean absolute error: 0.437
- Mean Absolute Percentage Error: 0.007
- Maximum Error: 3.10
- $`R^2`$ Score: 0.995

## Limitations

The model has been tested on annual data from a number of different countries over a period from 2000-2015. This covered a number of natural disasters however it may not be appropriate outside this context.

## Trade-offs

The training set contains more developing economies and so the model displays a natural bias.
