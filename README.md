# Bicycle-mode
Prediction Model of Bicycle mode choice model using Decision trees

Develop a Bicycle mode choice model using Decision trees based on the data attached. Prepare a prediction model (Yes/No) based on socioeconomic characteristics and trip conditions. Consider training data as 70% of the given data.

The first part of the questionnaire contains the socioeconomic characteristics, and the second part includes the questions for mode choice. The data has been given as an excel sheet. The missing values can be filled. Please communicate to clarify if you have any problems in interpreting the given data.

Steps for the solution:
1.	Given data is in the .xlsx format so we need to save it to .csv format.
2.	Next in PyCharm we need to import suitable libraries such as pandas, matplotlib, sklearn and numpy.
3.	Then we can go ahead and read the .csv file and print the head with 10 rows for a gist of the data.
4.	While converting there may be some extra rows and columns and we need to delete it.
5.	After that we have to rename the columns for easy handling of data. Updated column names:
		'Age'
		'Gender'
		'Education'
		 'Income'
		"Occupation"
		"Priv_Vehicle"
		"HH_Size"
		"Travel Time"
			"Type"
		"Scenario_1"
		"Scenario_2"
		"Scenario_3"
		"Scenario_4"
6.	Now we can check for the NaN values and data type for each column.
7.	7.	In order to run the machine learning algorithm, we have to convert all the required values of the data into integer or float data type instead of the existing string data type in some columns.
8.	We can do this by replacing specific values with numerical values such as 0, 1, 2, etc.
9.	For each column there are several NaN values we have to deal with so that the algorithm can give precise results. Here I have used the mean of each column to fill the NaN values so that it lies in the range of the given data.
10.	We can print the head of the data for the updated values.
11.	11.	Next, we create a column regarding the prediction value which will be calculated using the machine learning algorithm. I added the results of all the four scenarios and scaled the values of the “Predict” column from 0 to 4 to 0 to 1.
12.	Now we can import the libraries needed for the decision tree model.
13.	Then we define the independent columns or the feature columns in the given data.
14.	We can do the same for the target variable which is the “Predict” column.
15.	Now we create a training and testing dataset for both the dependent and independent variable.
16.	We choose 70% data for training and 30% data for testing as given in the question.
17.	We can now proceed to create a Binary Tree model on which we can fit the training data.
18.	We can check for the accuracy of the model using the testing dataset using this formula:
		Accuracy=(True Positive+True Negative)/(True Positive+False Positive+True Negative+False Negative)
19.	Precision score of the model can also be calculated. There are three types of precision score that I have calculated for this model. They are:
		•	Micro-averaged precision score
		•	Macro-averaged precision score
		•	Per-class precision score
20.	Similarly, we can also calculate the recall score.
21.	Then we can print the Confusion Matrix for the model.
22.	And after that we can print the classification report for the summary of the model.
