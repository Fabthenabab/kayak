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

Extract, transform and load cleaned data from your datalake to a data warehouse

## Dataset
Data on local accomodation is scraped from https://www.booking.com/
It contains : 
hotel name,
Url to its booking.com page,
Its coordinates: latitude and longitude
Score given by the website users
Text description of the hotel

The weather for each destination is fetched from https://openweathermap.org/api/one-call-api
The API helps determine the list of cities where the weather will be the nicest within the next 7 day 


### Build database
The dataset csv is stored in a data lake and converted in a SQL database


### Dependencies
- The source code is written in Python 3.
- The python packages can be installed with pip : `pip3 install -R requirements.txt`
  

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

