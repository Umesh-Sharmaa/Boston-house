# Boston House prediction

## Software and tools require

1. [GitHub Account](https://github.com)

2. [VS Code IDE](https://code.visualstudio.com/)

3. [Heroku](https://heroku.com)

4. [Git CLI](https://git-scm.com/downloads)

Create a new Environment

```
conda create -p venv python==3.11 -y
```
### Step 1: Create the model 
The prediction model is created on jupyter notebook by using kaggle's boston housing dataset. Mostly the house price prediction datasets have same features so you can use any dataset you want more or less the process is same.
So, firstly we load the data using pandas, then preprocessing it using different methods like Droping null values, finding correlation, Separating the target column from training data, etc. 
Preprocessing and data visualisation are important steps to find out the data correlation more accurately. However it depends upon the data that how much preprocessing it requires.
Once the preprocessing is done then it is very easy to split the data into training and testing data by using train test split.
Then using different models from sklearn for linear regression, train the models on training data and check their accuracy and root mean square error or root mean absolute error to find out which model gives most accurate predictions. 
Take the model with most accurate scores.

### Step 2: Load the model
Once the model is decided then simpliy save the model using pickle library.
This model will get used for further predictions anywhere we want in the project.
We also have to make sure that we should create an another model to perform the operatins on new data and make it ready for the prediction model as the new data is not exposed to normalization and reshape functions that will lead to an error by the prediction model.
Hence, at the end of this step we have two models, one for preprocessing and another for prediction.

### Step 3: Create a flask app
Now we have to create a flask app or if you want then you can have a django app totally depends.
This app will provide a basic interface to the end user to enter the input efficiently and will result an predicted output on the webpage that will help the user to see the result clearly.
We'll load both the models into the falsk app along with that a basic HTML form is get created, this form is the input interface for the end user.

### Setp 4: Deployment
After the flask application is successfully created, we'll deploy this app on render as it gives you 5 free deployments.
For that firstly upload the project on Github Repository using GIT CLI or Github directly.
Once the project is uploaded on github then go to render and connect the github repo with render.
After some time the deployment will get done.


## THANK YOU 
