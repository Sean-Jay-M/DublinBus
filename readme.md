# How To Run

## Prerequisites 

### Python 

To get started, you should [install Python](https://realpython.com/installing-python/)
on your system. Please install a version no less than 3.8.

After that, you should [install pip](https://pip.pypa.io/en/stable/installation/)
for managing python packages.

Be ensure to pip install the required packages listed in *requirements.txt*. It is best to do this in an environment. Some Packages will need to be installed in the global environment.

### Node.js and React 

Install [Node.js](https://nodejs.org/en/)

Run the following command in the *frontend* directory 

  npx create-react-app my-react-app

or

  npm install react

Be sure to npm install any required packages.

### PostgreSQL

Install both [PostgreSQL](https://www.postgresql.org/download/) and [PgAdmin](https://www.pgadmin.org/download/)

It is recommended to create a new PgAdmin account explicitly for this application.

## Setting Up The Backend

You must first set up a database and account within *PgAdmin*.

Within the *config/config.ini* file you must set the following parameters: 

- Key: This is your secret key, give it any value. This cannot change.
- Post: This is the path to the PostgreSQL database - postgresql://*AccountName*:*AccountPassword*@localhost:5432/*DatabaseName*
- Api: This is the API for accuweather, you must get your own key - http://dataservice.accuweather.com/currentconditions/v1/207931?apikey=*Key*

From here go to the directory where *run.py* is contained. Run the following commands:

  $ python
  
  $ from flask_react import DB 
  
  $ from flask_react.models import Weather
  
  $ db.create_all()
  
Now the table will be created within your *PostgreSQL* database.

From here you must run scraper.py. Depending on when you begin running this, it may not populate the table for up to 1 hour.

Finally run the file *run.py*.

## setting up the frontend 

Change to the directory *frontend* ensure you have npx installed React and the relevent modules. 

run the following command:

  $ npm start run
  
This will open up the application and run it.
