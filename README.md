# kayak
![Projet Kayak](/img/kayak-vector-logo.png)


## Objective
Create an application, similar to Kayak website, that will recommend where people should plan their next holidays.
The application should be based on real data about Weather and Hotels in the area.

The application should then be able to recommend the best destinations and hotels based on the above variables at any given time.
Application will focus first on the best cities to travel to in France. According One Week In.com here are the top-35 cities to visit in France:
https://one-week-in.com/35-cities-to-visit-in-france/


Get weather data from each destination
Get hotels' info about each destination
Store all the information above in a data lake
Extract, transform and load cleaned data from your datalake to a data warehouse

## Dataset
Dataset is scraped from Booking.com
The dataset is built from the [MIMIC-III dataset](https://mimic.physionet.org/) [1].

## Prerequisites
<!-- https://app.jedha.co/course/project-plan-your-trip-with-kayak-ft/plan-your-trip-with-kayak-ft -->

### Build database

Marketing team wants to focus first on the best cities to travel to in France. According One Week In.com here are the top-35 cities to visit in France:

- Request access to the MIMIC-III dataset : https://mimic.physionet.org/gettingstarted/access/
- Download the MIMIC-III GitHub repository : https://github.com/MIT-LCP/mimic-code/
- Follow instructions to build the SQL database : https://github.com/MIT-LCP/mimic-code/tree/master/buildmimic/postgres
- Build an additional table. This will create a psql table named rrt : 
```cd mimic-code/concepts/ 
psql -U postgres -d mimic -a -f rrt.sql
```

### Dependencies
- The source code is written in Python 3.
- The python packages can be installed with pip : `pip3 install -R requirements.txt`
- To use Keras models, first install tensorflow : https://www.tensorflow.org/install/
- WARNING : XGBoost installation with pip is currently disabled for Windows. Instructions for Windows users : https://xgboost.readthedocs.io/en/latest/build.html

## Usage
### Make_dataset.ipynb 
**Extracts the dataset from the SQL database**
- Input file : features_info.csv
- Output file : dataset_with_labels.csv (not hosted on this repository, you have to create it yourself)

### Explore_dataset.ipynb
**Automates some computations of basic statistics and plots for each feature in the dataset**
- Input file : 
### Train_models.ipynb
**Trains some multiclass classifiers from different packages (scikit-learn, keras, XGBoost) and compare their performances**
- Input file : 

## Team contributors

