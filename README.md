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

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/8c9d3ce1-98bf-43d3-aada-2a22933c9db8)

## Evaluation

We evaluate the model's performance using standard regression metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R2), providing insight into its predictive accuracy.

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/d86bff7f-96c5-40c7-9868-aa405348ce19)

## Interpretation

We analyze feature importance, visualize results, and create various plots and graphs to understand the relationship between features and the target variable, facilitating the model's interpretation.

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/60d88998-3962-4f92-a658-6ba8d7c4dd6a)

## Prediction of new data

We generate a new dataset of 8000 points across the country to predict the geothermal gradient for areas where there are no available data.

![image](https://github.com/jcmefra/Geothermal-Gradient-Machine-Learning/assets/64992303/6c6d476c-da05-4244-8563-d72f3d1e61f6)

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

This project explores the use of machine learning to predict geothermal gradients in specific regions. By leveraging a XGBoost regression model and carefully engineered features, we've made significant strides in understanding and predicting geothermal properties. While the model shows promise, there's room for further improvement and fine-tuning. We look forward to ongoing enhancements and potential applications in the field of geothermal exploration.

# Further Improvements

We aim to enhance the project by incorporating additional data sources to improve geothermal potential predictions. This could involve adding more geological data from wells or stratigraphic columns, structural data such as faults, permeability and porosity data, geochemical indicators, and real-time monitoring data. By expanding the dataset, we can refine our machine learning models for better accuracy in geothermal potential assessment.

Feel free to contribute to the project and help us improve geothermal exploration and energy generation.

## Sources:

   1. South American Moho dataset: Uieda, L., & Barbosa, V. C. (2017). Fast nonlinear gravity inversion in spherical coordinates with application to the South American Moho. Geophysical Journal International, 208(1), 162-176.
   2. Geothermal Gradients dataset: Alfaro, C., Alvarado, I., Quintero, W., Hamza, V., Vargas, C., & Briceño, L. (2009). Mapa preliminar de gradientes geotérmicos de Colombia. Proyecto Mapa Geotérmico de Colombia, 34.
   3. Volcanos dataset: Gómez-Tapias, J., Montes-Ramírez, N., Nivia, A., & Diederix, H. (2015). Mapa geológico de Colombia. Escala, 1:1.000.000.
   4. LAB depth dataset: Afonso, J. C., Salajegheh, F., Szwillus, W., Ebbing, J., & Gaina, C. (2019). A global reference model of the lithosphere and upper mantle from joint inversion and analysis of multiple data sets. Geophysical Journal International, 217(3), 1602-1628.
   5. Magnetic data: Lesur, V., Hamoudi, M., Choi, Y., Dyment, J., & Thébault, E. (2016). Building the second version of the world digital magnetic anomaly map (WDMAM). Earth, Planets and Space, 68, 1-13.
