==================================================================
Getting and Cleaning Data - Course Project
==================================================================
jagodag
25.01.2015
==================================================================
That excerices was carried out on purpose of Course Project of Getting and Cleaning Data, Coursera.

Description of experiment:

"The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. "


There were following tasks to be performed:
======================================
You should create one R script called run_analysis.R that does the following:
1.Merges the training and the test sets to create one data set.
2.Extracts only the measurements on the mean and standard deviation for each measurement. 
3.Uses descriptive activity names to name the activities in the data set
4.Appropriately labels the data set with descriptive variable names. 
5.From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.


To get the above I followed below steps:
=========================================

- read X_test data into R ( table called Xtest) - shows all the measurements' results ( of test data)
- read X_train data into R ( table called Xtrain) - shows all the measurements' results ( of train data)
- read y_test data into R ( table called ytest) - this represents activity index
- read y_train data into R ( table called ytrain) - this represents activity index
- read subject_test into R ( table called subjecttest) - subject index
- read subject_train into R (table called subjecttrain) - subject index
- to merge all data together so it makes sense, first we want to combine columns of ytest,subjecttest,Xtest; then merge columns of ytrain,subjecttrain, Xtrain; because both test and training data sets include the same number of features and measurememnts we can rbind them.
- Lets call merged data set 'data'
- Now we want to find out what features there are, and assign their names to columns in data. To do that, read features.txt into R ( table called features).
- Names that we are looking for are in the second column of features data set. Create listofNames being characteristic representation of the second column elements. ( as.character) Because we might get some duplicates, set unique = TRUE. This will make sure that all the names will be unique.
- Let's change data column names. First column is index of our activities, therefore column name will be Activity. The second column is Subject and all the remaining columns will get names saved under listOfNames ( obviously the order and number of names is the same).
- For the next step we will use dplyr library.
- We're looking for those columns that contain "mean.." in the name - assign it to data_mean ( using select and contain functions)
- We're looking for those columns that contain "std.." in the name - assign it to data_std
- Let's extract also columns that show activity and subject indexes - assign it to data_subj_act
- Let's merge three of the above data sets using cbind cbind(data_subj_act,data_mean,data_std) - assign it to subdata
- Read "activity_labels.txt" to get activities names - assign it to activities.
- Now we need to merge sudbdata with activities so to get appropriate activities names for each index. We need to merge it by "V1" from activities and "Activity" from subdata.
- Now when data is merged we want to get rid of activity indexes, as they are unnecessary ( get rid of first column) - subdataFinal
- We need to rename column that has got activities names to "Activity" and we get tidy data subdataFinal data set.
- To calculate mean of each feature we're going to use plyr package and apply ddply function.
- We want to calculate mean for each of the feaures for each Subject and Activity, therefore : a<- ddply(subdataFinal,.(Subject,Activity),numcolwise(mean))
- Just to be pedantic, we're going to ammend variables names so it is clear that we calculated the average values - we're going to add "avg_" to each of the variable names ( columns 3 : 69; ncol(a) will tell you how many columns they are)
  colnames(a) <- c("Subject","Activity",sub("^", "avg_", colnames(a)[3:69] ))
- a is our final data set that is required for step 5.


The dataset includes the following files:
=========================================

- 'README.txt'
- run_analysis.R
- codebook of variables 



Notes: 
======


License:
========
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
