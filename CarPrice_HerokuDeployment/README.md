# Car-Price-Prediction
# [Tutorial by Krish]("https://www.youtube.com/watch?v=p_tpQSY1aTs")
# [Kaggle Dataset]("https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho")


# Aim: to predict the selling price of cars to be sold

# Requirements: 
## Create a new environment for this project
## conda create -n env_name python=3.7 anaconda
## conda activate env_name
## conda install -n env_name
## install required libraries


# Steps followed:
## 1. Importing data
## 2. Cleaning data and data exploration
## 3. Feature engineering (choosing required features)
## 4. Data visualization
## 5. Finding if there exists corr among variables
## 6. train test split
## 7. Model building and Hyper-parameter tuning
## 8. using various sklearn.metrics : mean_absolute_error, mean_squared_error, np.sqrt(mean_squared_error)
## 9. converting the model to pickle file for future use



# Deployment:
## About Heroku and steps for deployment of a machine learning end-to-end project on this cloud PaaS:
    - Heroku is the first cloud platform as a service (PaaS)

    - As a pre-requisite, we need to fill the requirements.txt file. We can use the below command to find the environment's current package list installed in our system and accordingly fill the requirements.txt: 
	    pip freeze > requirements.txt

    - need to define set of processes/commands that should run beforehand into file named "Procfile"
	    web: gunicorn app:app
	    * web command tells Heroku to start a web server for the application, using gunicorn, 
        * The Gunicorn "Green Unicorn" is a Python Web Server Gateway Interface HTTP server which is used for running our python application instance. 
	    * Our application's name is app.py, we thus set app name to be app as well

    - Inside Heroku:
        * create your account
        * connect with github (provide read/write accesses to all your repositories)
        * provide the repository name to connect
        * Then deploy the github branch (master or if anything else). Once deployed, click on "view" to see the deployment.
        * If required (as atmax 5 projects can be deployed), delete the previously created apps from "Settings" tab.
        * via heroku terminal (which we can download from Heroku website), we can login to see the logs:
            > heroku login
            > heroku logs --app="app_name" > logs_appname.txt
