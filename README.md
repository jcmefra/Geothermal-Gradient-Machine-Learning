# Geothermal Gradient Prediction Project

# Table of Contents

1. [About the Project](#about-the-project)
2. [Methodology](#methodology)
3. [Getting Started](#getting-started)
4. [Conclussions](#conclusion)
5. [Further Improvements](#further-improvements)

# About the Project

This Project is aimed at predicting geothermal characteristics for Colombia, specifically the geothermal gradient, based on available geological and well data. We employ machine learning techniques to make these predictions. This project focuses on predicting the Apparent Geothermal Gradient (°C/Km) as an essential factor in geothermal exploration. The code and the results are in Model.ipynb.

# Methodology:

The project utilizes geospatial data, including well locations, geological information, and geothermal measurements. These datasets are located in the `data` folder of this repository. The data includes information on well depths, temperatures, geological features, and proximity to volcanic structures.

## ETL (Extract, Transform, Load)

The ETL phase involves importing the necessary datasets and performing initial preprocessing. This step ensures that the data is in the right format for further analysis.

## Feature Engineering

In this phase, we create new relevant features, such as computing distances to volcanoes and estimating Moho depth, which can significantly impact geothermal gradient prediction.

## Data Cleaning

Data cleaning involves removing irrelevant or incomplete records and columns to obtain a clean and structured dataset for machine learning.

## Machine Learning

We use a RandomForestRegressor to train a machine learning model that predicts apparent geothermal gradients based on the chosen features. The model's hyperparameters are tuned for optimal performance.

## Evaluation

We evaluate the model's performance using standard regression metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R2), providing insight into its predictive accuracy.

## Interpretation

We analyze feature importance, visualize results, and create various plots and graphs to understand the relationship between features and the target variable, facilitating the model's interpretation.

# Getting Started

Before running the project, you'll need to set up your Python environment and install the required dependencies. Here are the steps to get started:

1. Create a Conda environment (if not already created):
   
   conda create --name geothermal-predict python=3.7


2. Activate the Conda environment:

   conda activate geothermal-predict


3. Install pip within the Conda environment:

   conda install pip


4. Install the required Python packages using the provided `requirements.txt` file:

   pip install -r requirements.txt

Now your environment is set up, and you're ready to run the project code.

# Conclusion

This project explores the use of machine learning to predict geothermal gradients in specific regions. By leveraging a Random Forest regression model and carefully engineered features, we've made significant strides in understanding and predicting geothermal properties. While the model shows promise, there's room for further improvement and fine-tuning. We look forward to ongoing enhancements and potential applications in the field of geothermal exploration.

# Further Improvements

We aim to enhance the project by incorporating additional data sources to improve geothermal potential predictions. This could involve adding more geological data from wells or stratigraphic columns, structural data such as faults, permeability and porosity data, geochemical indicators, and real-time monitoring data. By expanding the dataset, we can refine our machine learning models for better accuracy in geothermal potential assessment.

Feel free to contribute to the project and help us improve geothermal exploration and energy generation.

## Credits:

   1. South American Moho dataset: Uieda, L., & Barbosa, V. C. (2017). Fast nonlinear gravity inversion in spherical coordinates with application to the South American Moho. Geophysical Journal International, 208(1), 162-176.
   2. Geothermal Gradients dataset: Alfaro, C., Alvarado, I., Quintero, W., Hamza, V., Vargas, C., & Briceño, L. (2009). Mapa preliminar de gradientes geotérmicos de Colombia. Proyecto Mapa Geotérmico de Colombia, 34.
   3. Volcanos dataset: Gómez-Tapias, J., Montes-Ramírez, N., Nivia, A., & Diederix, H. (2015). Mapa geológico de Colombia. Escala, 1:1.000.000.