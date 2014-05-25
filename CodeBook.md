This file describes the variables, the data, and any transformations or work that I performed to clean up the data.

Script "run_analysis.R" does the following steps to clean the data:
1. Reads X_train.txt, y_train.txt and subject_train.txt from the "./data/train" folder and stores them in trainData, trainLabel and trainSubject variables.
2. Reads X_test.txt, y_test.txt and subject_test.txt from the "./data/test" folder and stores them in testData, testLabel and testsubject variables.
3. Merges testData and trainData to generate a data frame called "joinData""; merges testLabel and trainLabel to generate a data frame called "joinLabel""; merges testSubject and trainSubject to generate a data frame called joinSubject.
4. Reads the features.txt file from the "/data" folder and store the data in a variable called "features". Extracts only the measurements on the mean and standard deviation and puts them into "joinData".
5. Cleans the column names of the "joinData". Removes the "()" and "-" symbols in the names, and makes the first letter of "mean" and "std" a capital letter "M" and "S".
6. Reads the activity_labels.txt file from the "./data"" folder and stores the data in a variable called "activity".
7. Cleans the activity names in the second column of "activity". Makes all names to lower cases. If the name has an underscore between letters, removes the underscore and capitalize the letter immediately after the underscore.
8. Transforms the values of joinLabel according to the activity data frame.
9. Combines joinSubject, joinLabel and joinData by column to get a new cleaned data frame called "cleanedData'. Names the first two columns, "subject" and "activity".
10. Writes the cleanedData out to "merged_data.txt" file in current working directory.
11. Generates a second tidy data set with the average of each measurement for each activity and each subject.
12. Writes the result into "data_with_means.txt" file in current working directory.
