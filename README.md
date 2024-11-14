# AI Hackathon for Livestock Data

## Code Explanation

#### 01 - data_preparation.ipynb

Description: 

This notebook handles data preparation and filtering processes, which includes loading the datasets, cleaning and organizing them, and performing initial feature engineering steps. 
All available data from 2017 to 2023 are integrated and filtered to focus on relevant columns and animal records.


Main Steps:
* Data loading and merging across sources
* Feature engineering for key metrics
* Data filtering

Output:
* A clean dataset ready for model training

#### 02 - model_search.ipynb

Description: 

This notebook performs the model search using the H2O library. It runs on an HPC cluster at DIBAF-UNITUS to select the best-performing model for predicting the reproductive metric DaysOpen. 
The search explores a range of ML-algorithms and configurations over a 20-hour runtime.


Main Steps:
* Initialization of the H2O environment
* Automated model training with H2O-AutoML functionality
* Generation of a leaderboard of model performances

Output: 
* The top-performing model and its parameters, saved for later evaluation

#### 03 - model_kfold.ipynb

Description: 

This module implements a 5-fold cross-validation for performance evaluation on the top-selected model from the model search. 
Using the sklearn library, this script verifies model stability and generalizability.


Main Steps:
* Setting up the k-fold cross-validation
* Training and validating the model across folds
* Recording performance metrics and analyzing feature importance

Output: 
* Cross-validation metrics for model performance and feature importance analysis

## Setup

* Python v. 3.x
* Pandas v. 2.0.1
* Numpy v. 1.23.5
* Matplotlib v. 3.7.1
* Seaborn v. 0.12.2
* Datetime 
* H2O v. 3.40.0.4
* Sklearn v. 1.2.2
* Pickle

## Requirements

The following datasets were selected as inputs for the analysis, each covering data from 2017 to 2023 and downloaded in CSV format:
* [parto.csv](https://opendata.leo-italy.eu/portale/dataset-info/61e0a4378e6e3b04221fdeba)
* [anagrafica.csv](https://opendata.leo-italy.eu/portale/dataset-info/61e146298e6e3b0422200495)
* [clima.csv](https://opendata.leo-italy.eu/portale/dataset-info/6245b6ee8e6e3b042235c122)
* [lattazione.csv](https://opendata.leo-italy.eu/portale/dataset-info/6418616825904da4bced9372)

## Built With

* [Python](https://www.python.org/) - The programming language used for the project.

## Authors

* **Davide Del Buono** email: davide.delbuono@unitus.it
* **Chiara Arcuri** email: chiara.arcuri@unitus.it
* **Giovanni Vignali** email: giovanni.vignali@unitus.it
* **Marco Milanesi** email: marco.milanesi@unitus.it
* **Daniele Pietrucci** email: daniele.pietrucci@unitus.it
* **Giovanni Chillemi** email: gchillemi@unitus.it

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
