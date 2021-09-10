# ML Pipeline for Short-Term Rental Prices in NYC - Udacity
This is the final project for the Lesson 3 of the Machine Learning DevOps Nanodegree.
Here we estimate the typical price for a given property based on the price of similar properties. We also receive new data in bulk every week so the model needs to be retrained with the same cadence, for this an end-to-end pipeline has been created.

## Instructions

The pipeline can be run by using  the ``main.py`` file in the root directory with MLflow.
Each individual step can be run by passing the step name as an argument to MLflow.

## Steps

### Data download and cleaning

This can be done by the steps "download" and "basic_cleaning". The en result is a `clean_sample.csv` artifact with price and location outliers removed.

### Data testing
This step "data_check" performs various tests on new input data to check for correct structure and feature values.

### Data split
This step called "data_split" uploads 2 new datasets artifacts `trainval_data.csv` and `test_data.csv` to WandB.

### Train Random Forest
With the "tran_random_forest" step we construct an Sklearn Pipeline that preprocesses input data and trains a Random Forest Regressor for predicting house price data.

## Results

### Visualizing the pipeline
The root Github directory contains a `graph_view.png` file with a graphical representation of the whole pipeline.

### Release
The latest working version can be found as a release in the repository.


