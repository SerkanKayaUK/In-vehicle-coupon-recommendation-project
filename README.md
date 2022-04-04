## In vehicle coupon recommendation project : Classification Model

####                             (c) Serkan Kaya - 1 April 2022

This is a Classification Machine Learning Model on the "in-vehicle coupon recommendation dataset" from the UCI Machine Learning repository (https://lnkd.in/dqBHNXCT).
For this project, I have estimated accuracy by using Logistic regression, KNN, Decision Tree, Random Forest, SVM, GBM, LightGBM, CatBoost Classifiers from sklearn,
catboost, lightgbm ML libraries in Python.

### Business Problem:
----------------------
This project studies whether a person will accept the coupon recommended to him in different driving scenarios.

### Dataset History:
--------------------   
This data was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather,
passenger, etc., and then ask the person whether he will accept the coupon if he is the driver.

### Source:
------------
Tong Wang, tong-wang '@' uiowa.edu, University of Iowa
Cynthia Rudin, cynthia '@' cs.duke.edu, Duke University

For more information about the dataset, please refer to the paper:
Wang, Tong, Cynthia Rudin, Finale Doshi-Velez, Yimin Liu, Erica Klampfl, and Perry MacNeille.
'A bayesian framework for learning rule sets for interpretable classification.'
The Journal of Machine Learning Research 18, no. 1 (2017): 2357-2393.


### Variables:
-----------------
There 25 variables (+1 Target variable: 'Y' ) and 12684 observations.


_destination:_ No Urgent Place, Home, Work.

_passanger:_ Alone, Friend(s), Kid(s), Partner (who are the passengers in the car).

_weather:_ Sunny, Rainy, Snowy.

_temperature:_ 55, 80, 30.

_time:_ 2PM, 10AM, 6PM, 7AM, 10PM.

_coupon:_ Restaurant(<$20), Coffee House, Carry out & Take away, Bar, Restaurant($20-$50).

_expiration:_ 1d, 2h (the coupon expires in 1 day or in 2 hours).

_gender:_ Female, Male.

_age:_ 21, 46, 26, 31, 41, 50plus, 36, below21.

_maritalStatus:_ Unmarried partner, Single, Married partner, Divorced, Widowed.

_has_Children:_ 1, 0.

_education:_ Some college - no degree, Bachelors degree, Associates degree, High School Graduate, Graduate degree (Masters or Doctorate), Some High School.

_occupation:_ Unemployed, Architecture & Engineering, Student, Education&Training&Library, Healthcare Support, Healthcare Practitioners & Technical, Sales & Related,
              Management, Arts Design Entertainment Sports & Media, Computer & Mathematical, Life Physical Social Science, Personal Care & Service, Community & Social Services,
              Office & Administrative Support, Construction & Extraction, Legal, Retired, Installation Maintenance & Repair, Transportation & Material Moving,
              Business & Financial, Protective Service, Food Preparation & Serving Related, Production Occupations, Building & Grounds Cleaning & Maintenance,
              Farming Fishing & Forestry.
            
_income:_ $37500 - $49999, $62500 - $74999, $12500 - $24999, $75000 - $87499, $50000 - $62499, $25000 - $37499, $100000 or More, $87500 - $99999, Less than $12500.

_Bar:_ never, less1, 1\~3, gt8, nan4\~8 (feature meaning: how many times do you go to a bar every month?)

_CoffeeHouse:_ never, less1, 4\~8, 1\~3, gt8, nan (feature meaning: how many times do you go to a coffeehouse every month?)

_CarryAway:_ n4\~8, 1\~3, gt8, less1, never (feature meaning: how many times do you get take-away food every month?)

_RestaurantLessThan20:_ 4\~8, 1\~3, less1, gt8, never (feature meaning: how many times do you go to a restaurant with an average expense per person of less than $20 every month?)

_Restaurant20To50:_ 1\~3, less1, never, gt8, 4\~8, nan (feature meaning: how many times do you go to a restaurant with average expense per person of $20 - $50 every month?)

_toCoupon_GEQ5min:_ 0,1 (feature meaning: driving distance to the restaurant/bar for using the coupon is greater than 5 minutes)

_toCoupon_GEQ15min:_ 0,1 (feature meaning: driving distance to the restaurant/bar for using the coupon is greater than 15 minutes)

_toCoupon_GEQ25min:_ 0,1 (feature meaning: driving distance to the restaurant/bar for using the coupon is greater than 25 minutes)

_direction_same:_ 0, 1 (feature meaning: whether the restaurant/bar is in the same direction as your current destination)

_direction_opp:_ 1, 0 (feature meaning: whether the restaurant/bar is in the same direction as your current destination)

_Y:_ 1, 0 (whether the coupon is accepted)

