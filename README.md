# Airline_Passenger_Referral_Prediction
## Problem Statement:
Airline Passenger Referral Prediction is a binary classification problem, that needs to predict whether a passenger will refer or recommend their known people to a particular airline for travel.
This dataset has almost all the datatypes. It includes numerical, categorical, text, and date data.
We have different rating features and customer reviews to predict the target variable. 
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

![image](https://github.com/balaji-89/Airline_Passenger_Referral_Prediction/assets/57706260/f1dd1883-d34c-4ed9-b108-e965d1d7e16e)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## What I did?

I started by changing the date features from object to datetime datatype. I created two features from the route which are visited_from and visit_to. After creating two features, I imputed the missing value of different rating features, by finding the average value of that respective airline and replacing NaN with that.

Then I found some columns with more Nan values that cannot be imputed. So I dropped that column. And then, I need to handle some categorical features now, I one_hot_encoded the airline features and then I also did the same trick with the cabin features.
Then I dropped the drown_date features. Then I have review data to handle, I made the entire review data lowercase, then removed punctual, stopping words and extra white spaces.

I used the TfidVector to change the text data into numerical, I chose 400 as the maximum features so each review observation will be converted into 400 length features.
I tried three different models SVC, RandomForest, and XGBoost for training. Among these RandomForest, XGBoost almost gave better results with the default parameters. 
Using the hyperparameter tuning doesn't make much difference. I chose SVM as the final model. I used GridSearch's API for finding the feature's importance and plotted it.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## Library Used:
- Sklearn
- Numpy
- Pandas
- Scipy
- Matplotlib

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png) 
## Execution Instructions:

1. Clone the repository:

   ```
   git clone https://github.com/balaji-89/Airline_Passenger_Referral_Prediction.git
   ```

2. Run :
      open file under src/models/PassengerReferral.ipynb, then run it cell by cell
   
Feel free to modify and adapt the content according to your project's specific details and requirements.





