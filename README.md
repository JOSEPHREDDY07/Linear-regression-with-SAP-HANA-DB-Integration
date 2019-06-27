# Linear-regression-with-SAP-HANA-DB-Integration
Data Analysis & Prediction using Python on SAP HANA Table data
This blog helps to integrate with SAP HANA DB (Version 1.0 SPS12) then extract the data from HANA table/View and 
analyze the data using Python Pandas library. Then you can clean and select independent variables/features data to 
feed the Machine learning algorithms to predict dependent variables or find insights.
In today’s digital economy, businesses cannot take action on stale insights, thus a true in-memory data 
platform should support real-time processing for transactions and analytics for all of a company’s data. 
SAP HANA helps to manage data in a single in-memory platform, so you can take action in the moment. 
Accelerate the pace of innovation and run live in this new digital economy. SAP HANA Capabilities include database services, 
advanced analytics processing, app development, data access, administration, and openness.

Python is becoming popular in analytics and data science. 
It is also portable, free, and easy .
Python lets you work quickly and integrate systems more effectively Python downloads with a large library 
that you can use so you don’t have to write your own code for every single thing. There are libraries for
regular expressions, documentation-generation, unit-testing, web browsers, threading, databases, CGI, email,
image manipulation, and a lot of other functionality.


Scenario: I have the state wise startup company’s expenditure (R&	D Spend, Administration Spend, and Marketing Spend) and profit data. 
Goal is to predict the Profit for the given set of expenditure values. I am not explaining details about the
ML Algorithm and the parameter tuning here.By taking this small set of data, I would like to show the end to end process 
of Data extraction, analyzing, cleaning, feature selection, and applying machine learning model and finally write back 
the results,ML algorithm performance metrics to the HANA tables. 
The linear regression is the most commonly used model in research and business and is the simplest to understand, so using the with random forest regression method we will predict the Profit.
The basic steps involved in this process are:

1.	Check the HANA Table data and analyze it using SQL in HANA Studio/WEB IDE.
(Make sure you have required privileges to do DMLOperations on the tables in SAP HANA Database.)
2.	Import pyodbc, pandas, Sklearn, Matplotlib libraries in python.
3.	Create connection to HANA data base and execute required SQL.
4.	Extract the data into data frame object and start analyzing it in Python using pandas.
5.	Do the feature engineering, data cleaning, feed the final set of independent variables to Machine learning algorithm (Random Forest) to predict dependent variable.
6.	Store the Machine learning algorithm metrics in log table and also update the predicted value into the HANA Table.
