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

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/274d04e3-a2b8-4d6f-a39c-47c593e29a45)

## Machine Learning

We use a XGBoost Regressor to train a machine learning model that predicts apparent geothermal gradients based on the chosen features. The model's hyperparameters are tuned for optimal performance.

## Feature importance

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/8a19bc7e-5532-4d33-8d14-befba4544951)
![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/3b5bb38a-e788-45f9-9f5a-f0f72b50e25a)
![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/354cdb39-3c31-42ce-a445-6e7e4d6905fc)
![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/c7b1dfcd-4b06-478f-83f2-36485858a3de)

## Evaluation

We evaluate the model's performance using standard regression metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R2), providing insight into its predictive accuracy.

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/68304b9c-8869-45bb-abfc-f40b16540270)
![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/1bd1613f-0b01-4304-9992-aa570c533444)


## Interpretation

We analyze feature importance, visualize results, and create various plots and graphs to understand the relationship between features and the target variable, facilitating the model's interpretation.

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/7b94e518-1c60-4c3e-b01a-96b242dd9eb7)

### Prediction of new data

We generate a new dataset of 8000 points across the country to predict the geothermal gradient for areas where there are no available data.

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/a5974b9e-8207-41fc-8fdd-7bd79981bd3e)
![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/15cb0898-f2be-47a9-a1a3-9b480e81d6e8)

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

Uieda, L., & Barbosa, V. C. (2017). Fast nonlinear gravity inversion in spherical coordinates with application to the South American Moho. Geophysical Journal International, 208(1), 162-176.
Alfaro, C., Alvarado, I., Quintero, W., Hamza, V., Vargas, C., & Briceño, L. (2009). Mapa preliminar de gradientes geotérmicos de Colombia. Proyecto Mapa Geotérmico de Colombia, 34.
Gómez-Tapias, J., Montes-Ramírez, N., Nivia, A., & Diederix, H. (2015). Mapa geológico de Colombia. Escala, 1:1.000.000.
Afonso, J. C., Salajegheh, F., Szwillus, W., Ebbing, J., & Gaina, C. (2019). A global reference model of the lithosphere and upper mantle from joint inversion and analysis of multiple data sets. Geophysical Journal International, 217(3), 1602-1628.
Maus, S., Barckhausen, U., Berkenbosch, H., Bournas, N., Brozena, J., Childers, V., ... & Caratori Tontini, F. (2009). EMAG2: A 2–arc min resolution Earth Magnetic Anomaly Grid compiled from satellite, airborne, and marine magnetic measurements. Geochemistry, Geophysics, Geosystems, 10(8).
Gómez, J. & Montes, N.E., compiladores. 2020. Atlas Geológico de Colombia 2020. Escala 1:500 000. Servicio Geológico Colombiano, 26 hojas. Bogotá.​​
Veloza, G., Styron, R., Taylor, M., Mora, A., 2012, Active Tectonics of the Andes: An open-source archive for active faults in northwestern South America, GSA Today, vol. 22, no. 10, p. 4-10, doi: 10.1130/GSAT-G156A.1.
