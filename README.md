# DublinBus
A React - Flask web application which utilizes Machine Learning techniques and models to predict bus journey times with a 95.8% Accuracy.
This application was made over the course of a number of months with four individuals: 

[Sean-Jay-M](https://github.com/Sean-Jay-M)

[Oscardbf](https://github.com/Oscardbf)

[Zaur Gouliev](https://github.com/gouliev)

[abotemper](https://github.com/abotemper)

## Branches
*Main:* The main branch contains the actual application as it was deployed, with the random forest models included.

*Data:* Contains code pertaining to the process by which the models were made.

*Testing:* The testing branch contains all the unit test and various other tests which were conducted. 

*Documentation:* The documentation branch contains details on how to run this project locally and various images of the application.

## Application Architecture
![Architecture](https://github.com/Sean-Jay-M/DublinBus/blob/documentation/images/webStackImage.png)

The application makes use of a *React* Frontend whih provides the user interface and exclusively handles the *cookie features*. This is supported by a number of packages and other technologies in order to provide the frontend interface such as Bootstrap. 

The *Flask* application provides two services:

  - The Prediction API makes use of 246 prediction models which can give an approximate 2^24 predictions.
  - The Weather API provides utilizes information from a *PostgreSQL* database to provide current weather conditions

The *PostgreSQL* database is populated by the *Scraper.py* script. This script calls the static method *insertData* which belongs to the weather class to populate the database.

*AccuWeather* is scraped for weather data.

*Google Maps* Provides the API for map.

## Data Analytics
![Architecture](https://github.com/Sean-Jay-M/DublinBus/blob/documentation/images/dataAnalyticsTwo.png)

The data which we were provided with was done so on the requirement that the original dataset never left the provided servers. Due to this a technical stack for conducting Data Analysis, Cleaning and Model creation was made. The original dataset was a csv file, which was loaded line by line by a python script into a MySQL database due to memory constraints. In order to connect to the server's *Jupyter Notebooks* a Bash script was created which would allow users to connect to the notebooks using SSH from their local machine. Further scripts were used to standardize initial Data Cleaning such that each person analyzing the Data had a standardized starting point.

A number of models were reviewed including:
  - Linear Regression
  - Decision Tree
  - K-Nearest 
  - Artifial Neural Networks 
  - Random Forest Regressor

The *Random Forest Regressor* was chosen due to having the most optimal performance metrics of: 
- R^2: 0.958
- MAE: 129.710's
- MSE: 220.811's

## Notes
The Original Repository can be found here: 

[Dublin Bus App ](https://github.com/gouliev/dublinbusapp)
