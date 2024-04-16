# Geothermal Gradient Prediction Project

# Table of Contents

1. [About the Project](#about-the-project)
2. [Methodology](#methodology)
3. [Conclussions](#conclusion)
4. [Further Improvements](#further-improvements)

# About the Project

This Project is aimed at predicting geothermal characteristics for Colombia, specifically the geothermal gradient, based on available geological and geophysical data. We employ machine learning techniques to make these predictions. This project focuses on predicting the Apparent Geothermal Gradient (°C/Km) as an essential factor in geothermal exploration. The code and the results are in Model.ipynb.

# Methodology:

The project utilizes geospatial data, geophysical information, and geothermal measurements. These datasets are located in the `data` folder of this repository. The data includes information on well depths, temperatures, geological features, and proximity to volcanic structures.

## ETL (Extract, Transform, Load)

The ETL phase involves importing the necessary datasets and performing initial preprocessing. This step ensures that the data is in the right format for further analysis.

## Feature Engineering

In this phase, we create new relevant features, such as computing distances to volcanoes and estimating Moho depth, which can significantly impact geothermal gradient prediction.

## Data Cleaning

Data cleaning involves removing irrelevant or incomplete records and columns to obtain a clean and structured dataset for machine learning.

## Machine Learning

We use a XGBoost Regressor to train a machine learning model that predicts apparent geothermal gradients based on the chosen features. The model's hyperparameters are tuned for optimal performance.

## Evaluation

We evaluate the model's performance using standard regression metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R2), providing insight into its predictive accuracy. We also generate plots for feature importance, actual vs predicted, residuals, etc.

## Interpretation

We analyze feature importance, visualize results, and create various plots and graphs to understand the relationship between features and the target variable, facilitating the model's interpretation.

### Prediction of new data

We generate a new dataset of 8000 points across the country to predict the geothermal gradient for areas where there are no available data.

![Mapa_Final](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/80fe424c-1cd5-41b0-a0bc-532fd71253ac)

# Conclusions

The project explores the use of Machine Learning to predict the geothermal gradient in areas where wells do not exist and are difficult to access.
A favorable result was obtained, with an MAE of 2.68, an RMSE of 3.58, and an R-squared value of 0.55.
The major source of dispersion and error is found in the extreme values (high, mainly), which corresponds to the minority in the training data.
It is suggested that, with a larger amount of high geothermal gradient data, the model will have a much higher accuracy.

# Further Improvements

We aim to refine our machine learning models for better accuracy in geothermal potential assessment, improving the resolution and the quality of the datasets, do further variable analysis to reduce overfitting and replace features for more significant ones if possible.

Feel free to contribute to the project and help us improve geothermal exploration and energy generation.

## Full manuscript: 

The full manuscript can be accessed at https://doi.org/10.48550/arXiv.2404.05184. This is not the final version, as we are doing some minor tweaks as per peer review comments. Stay tuned!
