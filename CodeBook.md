
									DATA DICTIONARY
Notes: 
======
- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.


Subject   
	An identifier of the subject who carried out the experiment
	values : 1 - 30
Activity
	Activities that each subject performed
	1 WALKING

	2 WALKING_UPSTAIRS

	3 WALKING_DOWNSTAIRS

	4 SITTING

	5 STANDING

	6 LAYING

	
Features

	The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

	Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

	Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

	These signals were used to estimate variables of the feature vector for each pattern:  
	'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.
	tBodyAcc-XYZ
	tGravityAcc-XYZ
	tBodyAccJerk-XYZ
	tBodyGyro-XYZ
	tBodyGyroJerk-XYZ
	tBodyAccMag
	tGravityAccMag
	tBodyAccJerkMag
	tBodyGyroMag
	tBodyGyroJerkMag
	fBodyAcc-XYZ
	fBodyAccJerk-XYZ
	fBodyGyro-XYZ
	fBodyAccMag
	fBodyAccJerkMag
	fBodyGyroMag
	fBodyGyroJerkMag


The set of variables that were estimated from these signals are: 

mean(): Mean value
std(): Standard deviation
mad(): Median absolute deviation 
max(): Largest value in array
min(): Smallest value in array
sma(): Signal magnitude area
energy(): Energy measure. Sum of the squares divided by the number of values. 
iqr(): Interquartile range 
entropy(): Signal entropy
arCoeff(): Autorregresion coefficients with Burg order equal to 4
correlation(): correlation coefficient between two signals
maxInds(): index of the frequency component with largest magnitude
meanFreq(): Weighted average of the frequency components to obtain a mean frequency
skewness(): skewness of the frequency domain signal 
kurtosis(): kurtosis of the frequency domain signal 
bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
angle(): Angle between to vectors.

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:

gravityMean
tBodyAccMean
tBodyAccJerkMean
tBodyGyroMean
tBodyGyroJerkMean

Features that are selected to the final result table set are those that contain "mean.." or "std..":
"tBodyAcc.mean...X"  
"tBodyAcc.mean...Y"                   
"tBodyAcc.mean...Z"
"tGravityAcc.mean...X"
"tGravityAcc.mean...Y"                 
"tGravityAcc.mean...Z"                
"tBodyAccJerk.mean...X" 
"tBodyAccJerk.mean...Y"   
"tBodyAccJerk.mean...Z"              
"tBodyGyro.mean...X"   
"tBodyGyro.mean...Y"     
"tBodyGyro.mean...Z"             
"tBodyGyroJerk.mean...X"        
"tBodyGyroJerk.mean...Y"              
"tBodyGyroJerk.mean...Z"     
"tBodyAccMag.mean.."    
"tGravityAccMag.mean.."   
"tBodyAccJerkMag.mean.."              
"tBodyGyroMag.mean.."       
"tBodyGyroJerkMag.mean.."       
"fBodyAcc.mean...X"              
"fBodyAcc.mean...Y"                   
"fBodyAcc.mean...Z"    
"fBodyAccJerk.mean...X"   
"fBodyAccJerk.mean...Y"     
"fBodyAccJerk.mean...Z"               
"fBodyGyro.mean...X"       
"fBodyGyro.mean...Y"          
"fBodyGyro.mean...Z"           
"fBodyAccMag.mean.."                  
"fBodyBodyAccJerkMag.mean.."   
"fBodyBodyGyroMag.mean.."    
"fBodyBodyGyroJerkMag.mean.."     
"angle.tBodyAccJerkMean..gravityMean."
"tBodyAcc.std...X"           
"tBodyAcc.std...Y"       
"tBodyAcc.std...Z"    
"tGravityAcc.std...X"                 
"tGravityAcc.std...Y"          
"tGravityAcc.std...Z"      
"tBodyAccJerk.std...X"  
"tBodyAccJerk.std...Y"                
"tBodyAccJerk.std...Z"      
"tBodyGyro.std...X"      
"tBodyGyro.std...Y"   
"tBodyGyro.std...Z"                   
"tBodyGyroJerk.std...X"        
"tBodyGyroJerk.std...Y"    
"tBodyGyroJerk.std...Z" 
"tBodyAccMag.std.."                   
"tGravityAccMag.std.."      
"tBodyAccJerkMag.std.."      
"tBodyGyroMag.std.."        
"tBodyGyroJerkMag.std.."              
"fBodyAcc.std...X"             
"fBodyAcc.std...Y"          
"fBodyAcc.std...Z"       
"fBodyAccJerk.std...X"                
"fBodyAccJerk.std...Y"        
"fBodyAccJerk.std...Z"     
"fBodyGyro.std...X"       
"fBodyGyro.std...Y"                   
"fBodyGyro.std...Z"        
"fBodyAccMag.std.."    
"fBodyBodyAccJerkMag.std.."     
"fBodyBodyGyroMag.std.."              
"fBodyBodyGyroJerkMag.std.." 

Avergaes of the above variables are as follows:
"avg_tBodyAcc.mean...X"  
"avg_tBodyAcc.mean...Y"                   
"avg_tBodyAcc.mean...Z"
"avg_tGravityAcc.mean...X"
"avg_tGravityAcc.mean...Y"                 
"avg_tGravityAcc.mean...Z"                
"avg_tBodyAccJerk.mean...X" 
"avg_tBodyAccJerk.mean...Y"   
"avg_tBodyAccJerk.mean...Z"              
"avg_tBodyGyro.mean...X"   
"avg_tBodyGyro.mean...Y"     
"avg_tBodyGyro.mean...Z"             
"avg_tBodyGyroJerk.mean...X"        
"avg_tBodyGyroJerk.mean...Y"              
"avg_tBodyGyroJerk.mean...Z"     
"avg_tBodyAccMag.mean.."    
"avg_tGravityAccMag.mean.."   
"avg_tBodyAccJerkMag.mean.."              
"avg_tBodyGyroMag.mean.."       
"avg_tBodyGyroJerkMag.mean.."       
"avg_fBodyAcc.mean...X"              
"avg_fBodyAcc.mean...Y"                   
"avg_fBodyAcc.mean...Z"    
"avg_fBodyAccJerk.mean...X"   
"avg_fBodyAccJerk.mean...Y"     
"avg_fBodyAccJerk.mean...Z"               
"avg_fBodyGyro.mean...X"       
"avg_fBodyGyro.mean...Y"          
"avg_fBodyGyro.mean...Z"           
"avg_fBodyAccMag.mean.."                  
"avg_fBodyBodyAccJerkMag.mean.."   
"avg_fBodyBodyGyroMag.mean.."    
"avg_fBodyBodyGyroJerkMag.mean.."     
"avg_angle.tBodyAccJerkMean..gravityMean."
"avg_tBodyAcc.std...X"           
"avg_tBodyAcc.std...Y"       
"avg_tBodyAcc.std...Z"    
"avg_tGravityAcc.std...X"                 
"avg_tGravityAcc.std...Y"          
"avg_tGravityAcc.std...Z"      
"avg_tBodyAccJerk.std...X"  
"avg_tBodyAccJerk.std...Y"                
"avg_tBodyAccJerk.std...Z"      
"avg_tBodyGyro.std...X"      
"avg_tBodyGyro.std...Y"   
"avg_tBodyGyro.std...Z"                   
"avg_tBodyGyroJerk.std...X"        
"avg_tBodyGyroJerk.std...Y"    
"avg_tBodyGyroJerk.std...Z" 
"avg_tBodyAccMag.std.."                   
"avg_tGravityAccMag.std.."      
"avg_tBodyAccJerkMag.std.."      
"avg_tBodyGyroMag.std.."        
"avg_tBodyGyroJerkMag.std.."              
"avg_fBodyAcc.std...X"             
"avg_fBodyAcc.std...Y"          
"avg_fBodyAcc.std...Z"       
"avg_fBodyAccJerk.std...X"                
"avg_fBodyAccJerk.std...Y"        
"avg_fBodyAccJerk.std...Z"     
"avg_fBodyGyro.std...X"       
"avg_fBodyGyro.std...Y"                   
"avg_fBodyGyro.std...Z"        
"avg_fBodyAccMag.std.."    
"avg_fBodyBodyAccJerkMag.std.."     
"avg_fBodyBodyGyroMag.std.."              
"avg_fBodyBodyGyroJerkMag.std.." 








==================================================================
Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Universit� degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws
==================================================================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.


For more information about this dataset contact: activityrecognition@smartlab.ws

License:
========
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
