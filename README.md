# Airbnb New User Destination Prediction
The purpose of this project is to try to find a good model to predict the first destination of the new user of airbnb.  

## Introduction to Data
In train_user_2.csv and test_users.csv file, data provided a list of users along with some related information and statistics such as 
gender, language and signup flow. Sessions.csv file gives information about web sessions log for users. 
The column ‘country_destination’ in train file is the record of destination of each user and it is the target variable to predict 
in the test set. There are 12 possible outcomes of the destination countries: 
‘US’, ‘FR’, ‘CA’, ‘GB’, ‘ES’, ‘IT’, ‘PT’, ‘NL’,‘DE’, ‘AU’, ‘NDF’ (no destination found), and ‘other’. 
Countries.csv also provides information about 10 country destination. All users in test file are new user and are 
from the USA, therefore, we are required to predict which country their first booking destination will be.

The training and test sets are split by dates. The training set includes users dataset dates back to 2010 and in the test set, 
all the new users are people with first activities after 7/1/2014 . The following part gives a detailed description of variables in files.

### File descriptions  
1. train_users.csv - the training set of users  
2. test_users.csv - the test set of users id: user id; 
date_account_created: the date of account creation;   
timestamp_first_active: timestamp of the first activity, 
note that it can be earlier than date_account_created or date_first_booking because a user can search before signing up;   
date_first_booking: date of first booking;   
gender;  
age;  
signup_method: Users can choose to register directly or log in with facebook or google account;  
signup_flow: the page a user came to signup up from;   
language: international language preference;  
affiliate_channel: what kind of paid marketing;  
affiliate_provider: where the marketing is e.g. google, craigslist, other;  
first_affiliate_tracked: whats the first marketing the user interacted with before the signing up;  
signup_app: users can choose web, andrew, ios or Moweb as media to browse information on Airbnb;  
first_device_type: the phone or computer system that users use when they first browse Airbnb;  
first_browser: the browser the user used when browsing Airbnb for the first time;  
country_destination: this is the target variable you are to predict  
3. sessions.csv - web sessions log for users user_id: to be joined with the column ‘id’ in users table  
4. countries.csv - summary statistics of destination countries in this dataset and their locations  
5. age_gender_bkts.csv - summary statistics of users’ age group, gender, country of destination
