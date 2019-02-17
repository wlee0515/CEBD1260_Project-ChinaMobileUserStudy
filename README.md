# Application Criteria Generator

This project is for the course CEBD1260: Big Data Analytics.

## Objective

In this project, we will study the application usage database provided by China Mobile. The database provides a list of events listing the applications installed and in used in the client’s device. The database also provides information about the client device model and their associated user information (age, gender and location).

The expected outcome of this exercise is to be able to generate a set of topics targeted towards a set of audience to maximize user engagement.

## Data Source
https://www.kaggle.com/chinapage/china-mobile-user-gemographics/home

## Data Description
The data is generated  by an application developed by a company named TalkingData. Talking Data is a Chinese analytics company.

The provided data is the application usage of a device of TalkingData users starting from April 30th 2016 to May 7th 2016. The span of the data is 1 week.

This data was provided on Kaggle for the development of a user classification model that will predict the Age and Gender of the user.

The application will periodically return an event back to China Mobile with the following information:
  - Device id
  - A list of applications installed on the device
  - A list of applications that are active on the device
  - The location of the device
  - The time of event

In addition to the returned event China mobile has a list of user information associated on the device and the categories of each application.

The list of user information provided is as follow for the training set:
  - Device Brand
  - Device Model
  - User Age
  - User Gender

The list of user information provided is as follow for the test set:
  - Device Brand
  - Device Model

## Project Assumption
it is possible to maximise the engagement of an application if the application carries the same attributes of the interest of the user at a given time frame.

## Project Methodology
In order to generate a list of topics for the development of a new application, this project will use the provided data to monitor the interest level of a user base on the applications they are using. This is made possible because the database provides a list of applications that are installed and active on the user’s device in a periodic matter.

## Project Steps
  1) Take the application categories and generate a word vector that will describe the interest attribute of an application. This vector will be referred to as the “interest Vector”
  2) Aggregate the interest vector of each active application noted in each event to get an interest vector representing the interest of the user at the time and location of the event.
  3) Find a correlation between the user profile and the interest vector
  4) Model the correlation between the user profile and the interest vector to predict the interest vector of an artificial user profile.
  5) Find the list of application categories that correlates to the generated interested vector
  6) Rank the application categories base on the interest vector
  7) Recommend the ranked list of applications categories to the developer.




