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

The application makes use of a *React* Frontend whih provides the user interface and exclusively handles the *cookie features*

The *Flask* application provides two services:
  -The Prediction API makes use of 246 prediction models which can give an approximate 2^24 predictions.
  -The Weather API provides utilizes information from a *PostgreSQL* database to provide current weather conditions
  


## Notes
The Original Repository can be found here: 

[Dublin Bus App ](https://github.com/gouliev/dublinbusapp)
