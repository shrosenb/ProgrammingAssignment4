##Information on Attributes 

###For each entry:
Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
Triaxial Angular velocity from the gyroscope.
A 561-feature vector with time and frequency domain variables.
Activity name.
ID of the subject who carried out the experiment.

###Goal
From the UCI HAR Dataset downloaded from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip:
1. Merge the training and the test sets to create one data set. 
2. Extract only the measurements on the mean and standard deviation for each measurement. 
3. Use descriptive activity names to name the activities in the data set 
4. Appropriately label the data set with descriptive activity names. 
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

###Training & Test sets
The following text files were imported and merged. 
Column names were assigned when the files were imported, prior to merge. 
'features.txt'
'activity_labels.txt'
'subject_train.txt'
'x_train.txt'
'y_train.txt'
'subject_test.txt'
'x_test.txt'
'y_test.txt'

###Extracting mean and standard deviation
A logical vector was created.
TRUE for the ID, mean & stdev columns
FALSE for the others values.
Merged data kept only the relevant columns

###Rename activities for meaningful names
activity_labels.txt was merged with the subsetted data to add meaningful activity names.
'activityId' values were replaced with the matching 'activityType' values.

###Label dataset with activity names
Used 'gsub' to clean up the column names in the merged, subsetted data set. 
'activityType' column removed in order to tidy data further.

###Create the tidy dataset
New table was created which contains average for each variable for each activity and subject.
