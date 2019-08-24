
1/the first thing i made data preperation 
2/ then i downloaded the data from link provided at coursera
3/ after that ...
 3.1/ Assign each data to variables
      * features <- features.txt
      * activities <- activity_labels.txt
      * subject_test <- test/subject_test.txt
      * x_test <- test/X_test.txt
      * y_test <- test/y_test.txt
      * subject_train <- test/subject_train.txt
      * x_train <- test/X_train.txt
      * y_train <- test/y_train.txt     
 3.2/ Merges the training and the test sets to create one data set
      * X  is created by merging x_train and x_test
      * Y  is created by merging y_train and y_test
      * Subject  is created by merging subject_train and subject_test
      * Merged_Data (10299 rows, 563 column) is created by merging Subject, Y and X
 3.3/ Extracts only the measurements on the mean and standard deviation for each measurement
      * TidyData  is created by subsetting Merged_Data, selecting only columns: subject, code and the             measurements on the mean and standard deviation (std) for each measurement
 3.4/ Uses descriptive activity names to name the activities in the data set
      * Entire numbers in code column of the TidyData replaced with corresponding activity taken from             second column of the activities variable
 3.5/ Appropriately labels the data set with descriptive variable names
      * code column in TidyData renamed into activities
      * All Acc in column’s name replaced by Accelerometer
      * All Gyro in column’s name replaced by Gyroscope
      * All BodyBody in column’s name replaced by Body
      * All Mag in column’s name replaced by Magnitude
      * All start with character f in column’s name replaced by Frequency
      * All start with character t in column’s name replaced by Time
 3.6/ From the data set in step 4, creates a second, independent tidy data set with the average of each          variable for each activity and each subject
      * FinalData (180 rows, 88 columns) is created by sumarizing TidyData taking the means of each               variable for each activity and each subject, after groupped by subject and activity.
      * Export FinalData into FinalData.txt file.
4/ overview of the final shape
