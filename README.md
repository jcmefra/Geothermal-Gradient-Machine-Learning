# Geothermal Gradient Prediction Project

# Table of Contents

1. [About the Project](#about-the-project)
2. [Methodology](#methodology)
3. [Getting Started](#getting-started)
4. [Conclussions](#conclusion)
5. [Further Improvements](#further-improvements)

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

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/a5974b9e-8207-41fc-8fdd-7bd79981bd3e)

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

# Conclusions

The project explores the use of Machine Learning to predict the geothermal gradient in areas where wells do not exist and are difficult to access.
A favorable result was obtained, with a mean absolute error of 2.85°C/Km.
The major source of dispersion and error is found in the extreme values (high, mainly), which corresponds to the minority in the training data.
It is suggested that, with a larger amount of high geothermal gradient data (greater than 45°C/km), the model will have a much higher accuracy.

# Further Improvements

We aim to refine our machine learning models for better accuracy in geothermal potential assessment, improving the resolution and the quality of the datasets, do further variable analysis to reduce overfitting and replace features for more significant ones if possible.

Feel free to contribute to the project and help us improve geothermal exploration and energy generation.

## Sources:

- Uieda, L., & Barbosa, V. C. (2017). Fast nonlinear gravity inversion in spherical coordinates with application to the South American Moho. Geophysical Journal International, 208(1), 162-176.
- Alfaro, C., Alvarado, I., Quintero, W., Hamza, V., Vargas, C., & Briceño, L. (2009). Mapa preliminar de gradientes geotérmicos de Colombia. Proyecto Mapa Geotérmico de Colombia, 34.
- Gómez-Tapias, J., Montes-Ramírez, N., Nivia, A., & Diederix, H. (2015). Mapa geológico de Colombia. Escala, 1:1.000.000.
- Dyment, J., Choi, Y., Lesur, V., Garcia-Reyes, A., Catalan, M., Ishihara, T., ... & Hamoudi, M. (2020, May). The World Digital Magnetic Anomaly Map: version 2.1. In EGU General Assembly Conference Abstracts (p. 22098).
- Gómez, J. & Montes, N.E., compiladores. 2020. Atlas Geológico de Colombia 2020. Escala 1:500 000. Servicio Geológico Colombiano, 26 hojas. Bogotá.​​
- Veloza, G., Styron, R., Taylor, M., Mora, A., 2012, Active Tectonics of the Andes: An open-source archive for active faults in northwestern South America, GSA Today, vol. 22, no. 10, p. 4-10, doi: 10.1130/GSAT-G156A.1.
- NASA Visible Earth. (2021). Topography. Retrieved from https://visibleearth.nasa.gov/images/73934/topography
- Gómez, J. & Montes, N.E., compiladores. 2020. Mapa Geológico de Colombia en Relieve 2020. Escala 1:1 000 000. Servicio Geológico Colombiano, 2 hojas. Bogotá.
- Veloza, G., Styron, R., Taylor, M., & Mora, A. (2012). Open-source archive of active faults for northwest South America. Gsa Today, 22(10), 4-10.
- Sandwell, D. T., Harper, H., Tozer, B., & Smith, W. H. (2021). Gravity field recovery from geodetic altimeter missions. Advances in Space Research, 68(2), 1059-1072.
- Pavlis, N. K., Holmes, S. A., Kenyon, S. C., & Factor, J. K. (2012). The development and evaluation of the Earth Gravitational Model 2008 (EGM2008). Journal of geophysical research: solid earth, 117(B4).
- Camacho et al. (2014). MAPA DE PROFUNDIDAD A LA ISOTERMA DE CURIE PARA COLOMBIA 1:3250000. Servicio Geológico Colombiano. Bogotá.
