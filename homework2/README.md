This folder contains my submission for Homework 2 of the MLESS course.

## File structure
- Forecast model results are inside the /forecasts folder. This folder also includes the X_test_sample and y_test_sample csv files. All those are needed for plotting in Task_1.ipynb.
- Task_1, Task_2_MLP, Task_3_MLP are notebooks including code to the corrresponding task from the second homework assignment.

## My Contributions
- Added data exports for all forecast models.
- Solved Task 1 of the homework assignment by creating a compilation plot of all forecast models. I created a new Notebook Task_1 instead of using the existing Notebook 7, as I think this improves file structure clarity with one notebook per task.
- Solved Task 2 of the homework assignment by implementing a MLP accepting temperature and o3 as input and o3 as output.
- Solved Task 3 of the homework assignment by extending the MLP of Task 2 to also use future temperature values as input and comparing performance of Task 2 and 3 models.
- Included comments and markdown cells to document the code.

Below is the original description of the parent repository with the original description of the files.
---
# Timeseries analysis and forecasting based on TOAR data

The [Tropospheric Ozone Assessment Report (TOAR)](https://igacproject.org/activities/TOAR) is an international research activity to provide globally consistent information on the distribution and trends of the air pollutant ozone in the lower part of the atmosphere. Ozone impacts human health, vegetation, and climate, and TOAR provides the data and analyses to quantify the damage caused by ozone.

As the central data service, the [Jülich Supercomputing Centre](https://www.fz-juelich.de/en/ias/jsc) developed and operates the [TOAR Data Infrastructure](https://toar-data.fz-juelich.de/), which stores more than 420,000 time series of ozone and related chemical and meteorological variables. The TOAR data services use a REST API to allow users the download and analysis of custom-tailored datasets. Here, we will make use of this API to obtain and preprocess a couple of exemplary timeseries, which we then use as input data to various machine learning models to demonstrate various aspects around forecasting and interpolation.

The notebooks in this folder are structured as follows:
* 1_Download_Preprocess_data.ipynb: in this notebook, data are downloaded from the TOAR data infrastructure and repackaged so that it can be easily used in the machine learning models
* 2_Data_Analysis.ipynb: here, some visualisations and statistical analyses are demonstrated to gain insights into the data and inform decisions on how the data should be trated in the machine learning workflow
* 3_AutoRegressive_Models.ipynb: this notebook implements a classical statistical technique to establish a baseline against which the ML models can be compared
* 4_MLP.ipynb: here we  build a multilayer perceptron model for timeseries forecasting (**how about RNN?**)
* 5_LSTM.ipynb: this notebook demonstrates a more refined ML architecture for timeseries analysis and forecasting 
* 6_PatchTST.ipynb: finally, we demonstrate the use of a modern, transformer-based architecture for timeseries forecasting

Note that these notebooks focus primarily on monovariate forecasting tasks (i.e. one variable at a time), so they ignore possible correlations among different variables. Extension to multivariate models is left as an exercise to the reader.

Authors: Sindhu Vasireddy and Martin Schultz, Jülich, May 2025
