# A Method to Predict the Percentage of Biodegradation in Polymeric Materials

This repository contains the data and code used in the article "A Method to Predict the Percentage of Biodegradation in Polymeric Materials". The data is stored in CSV format and the analysis is performed in a Jupyter notebook.

## Introduction

This project aims to predict the percentage of biodegradation in polymeric materials using LSTM technique. The provided dataset includes experimental data for differents biodegradability materials.

## Dataset

The dataset is provided in the directory and consists of the following CSV files:

- `Data_Samples.csv`: Contains the experimental data used for the analysis.

The structure of `Data_Samples.csv` is as follows:

| Column Name     | Description                                  |
|-----------------|----------------------------------------------|
| Day             | Sequence of day the measurements were taken  |
| Sample          | Measured value                               |

The data is already balanced with the use of SMOTE

## Notebook

The analysis is conducted in a Jupyter notebook available in the `notebooks` directory:

- `Bio.ipynb`: This notebook includes the model training, and evaluation of the predictive models. 

Pre-processing on the data has already been done. 

## Repository

| File Name                       | Description                                        |
|---------------------------------|----------------------------------------------------|
| 'Sample_40bio.csv'              | Sequence of day the measurements were taken        |
| 'Sample_80bio.csv'              | Test sample with 40% biodegradability polymer      |
| 'Sample_100bio.csv'             | Test sample with 80% biodegradability polymer      |
| 'Data_Sample_Serie_Values.csv'  | Serialized values for training                     |
| 'Data_Samples.csv'              | Experimental data used for the analysis            |
|  model_saved                    | Trained model                                      |
|  `Bio.ipynb`                    | Python notebook                                    |

## Observations

Whenever we train a new model, the resulting values will be different due to a combination of factors intrinsic to the machine learning process. Firstly, random initialization of weights can lead to different optimization paths, resulting in varied solutions. Additionally, using regularization techniques such as dropout introduces an extra layer of variability, affecting how the model learns from the training data. Small changes to the input data or the order in which examples are presented can also have an impact. The combination of these elements creates a scenario where each training run, even under the same general conditions, generates a unique set of parameters, leading to variations in the values produced by the model. However, once the hyperparameters are adjusted, variations should be small without significant impact on the results.
