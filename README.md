# Linear-regression-with-SAP-HANA-DB-Integration

Data Analysis & Prediction using Python on SAP HANA Table data
This blog helps to integrate with SAP HANA DB (Version 1.0 SPS12) then extract the data from HANA table/View and analyze the data using Python Pandas library. Then you can clean and select independent variables/features data to feed the Machine learning algorithms to predict dependent variables or find insights.


Scenario: I have the state wise startup company’s expenditure (R&	D Spend, Administration Spend, and Marketing Spend) and profit data. 
Goal is to predict the Profit for the given set of expenditure values. I am not explaining details about the ML Algorithm and the parameter tuning here.By taking this small set of data, I would like to show the end to end process of Data extraction, analyzing, cleaning, feature selection, and applying machine learning model and finally write back the results, ML algorithm performance metrics to the HANA tables. 
The linear regression is the most commonly used model in research and business and is the simplest to understand, so using the with random forest regression method we will predict the Profit.

The basic steps involved in this process are:

1.	Check the HANA Table data and analyze it using SQL in HANA Studio/WEB IDE.
(Make sure you have required privileges to do DMLOperations on the tables in SAP HANA Database.)
2.	Import pyodbc, pandas, Sklearn, Matplotlib libraries in python.
3.	Create connection to HANA data base and execute required SQL.
4.	Extract all the historical data into data frame object and start analyzing it in Python using pandas.
5.	Do the feature engineering, data cleaning, feed the final set of independent variables to Machine learning algorithm (Random Forest) to predict dependent variable (Profit).
6.	Analyze the Machine learning algorithm metrics and fine tune for the better accuracy by repeating the step 5.Store the Machine learning algorithm metrics in log table and also update the predicted value of historical data into the HANA Table.
7.	For the new data set, create the python program which reads the new data using pyodbc connection and predict the dependent variable (Profit) and updates the actual transactional table for reporting.
8.	Schedule this program and keep monitoring the model metrics and predicted value.

When using Python IDE’s such as Jupiter, the data is persisted to the client with the above approach and this means more processing time when you have large data set, which leads to drop the productivity of Data Scientists.
This is where the SAP HANA Data Frame can add real value to a Data Scientist’s work. More features and capabilities are included in SAP HANA 2.0 SPS03 Version to analyze / address the data science use cases with Python driver (hdbcli) and then the Python Client API for machine learning algorithms.

https://medium.com/@josephreddy07/end-to-end-model-of-data-analysis-prediction-using-python-on-sap-hana-table-data-800614d956ca?postPublishedType=repub



