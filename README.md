### Getting and Cleaning Data Course Project

## Introduction

This repo contains the script and README.md for my course project for the Coursera "Getting and Cleaning Data" Class. The data for the class that the script is meant to run on can be downloaded from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and will be refered to as the "Samsug Dataset".

(The data used in the class originally came from this research project[1]: 
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

## The Samsung Dataset
The Samsung dataset contains pre-processed measurments from a group of 30 volunteers who each performed 6 activities while wearing a smartphone on the waist. The device`s accelerometer and gyroscope were used to capture linear acceleration and angular velocity. The dataset has also  been randomly partitioned into two sets: training data and test data.

The files included with the Samsung data are:
- `README.txt`: Information about the project and description of the data.
- `features_info.txt`: Shows information about the variables used on the feature vector.
- `features.txt`: List of all features.
- `activity_labels.txt`: Links the class labels with their activity name.
- `train/X_train.txt`: Training set.
- `train/y_train.txt`: Training labels.
- `test/X_test.txt`: Test set.
- `test/y_test.txt`: Test labels.
- `train/subject_train.txt`: Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 
- `test/subject_test.txt`: Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

Both the `train` and `test` data sets also include `Inertial Signals` folders with additional data. However these are not relevant for this project, and hence not discussed any further.

For a more through description of the Samsung data set, please refer to the README.txt included with the original data.


## run_analysis.R

The script takes the Samsung data set and performs the steps below to generate a single tidy data set. The tidy data set summarizes each measurement via its mean by subject and activity.

The `run_analysis.R` sript:
 * Loads and merges the training and the test sets to create a single data set.
 * Replaces the activity codes in the Samsung data with the corresponding activity names.
 * Labels the variables with descriptive variable names which match the names of the feature vectore form the Samsung data.
 * Extracts only the mean and standard deviation for each measurement form the feature vector. Measurments in the feature vector without a mean or standard deviation are discarded. 
 * Generates a second, independent tidy data set with the average of each variable by activity and subject and writes this data set to `course_project_tidyData.txt`.

To **run the script**, it should be executed from the same directory that contains the `README.txt` of the Samsung data set.

## Codebook

This section contains information on all the variables included in the output data set from the `run_analysis.R` script.

`activity`	(factor)  
>Label that indicates which of the 6 activities the subject was performing:  
>>WALKING  - walking   
    WALKING_UPSTAIRS  - walking up a et of stairs  
    WALKING_DOWNSTAIRS  - walking down a set of stairs  
    SITTING  - sitting  
    STANDING  - standing   
    LAYING  -  laying down

`subject`	(factor)  
>ID number indicating which subject the data was collected from.  
>>Ranges from 1 to 30

**All Other Variables** (numeric)  
>The dataset includes 66 other variables, these values are the MEAN (by subject and activity) of the __identically named__ feature variables in the orignal Samsung data set. These variables represent pre-processed measurements from the smartphone`s accelerometer (`Acc` in the variable name) and Gyroscope (`Gyro`) along all 3 axis (`-X, -Y, -Z` suffixes). All raw data from the phone was **captured in standard gravity units `g`**. 
>
>Data from the acceleromater has further been split into acceleration due to Gravity (`GravityAcc`) and acceleration due to movement of the subject`s body (`BodyAcc`). Jerk and magnitude signals were also calculated and included as `Jerk` and `Mag` in the variable name respectively. The `t` and `f` prefixes indicate time-domain vs. frequency domain signals.

>Full details, including what pre-processing procedures were applied, can be found in the `README.txt` and `features_info.txt` of the Samsung data set.

>The variables included in this output data set are:
>>`tBodyAcc-mean()-X`
>>`tBodyAcc-mean()-Y`
>>`tBodyAcc-mean()-Z`
>>`tBodyAcc-std()-X`
>>`tBodyAcc-std()-Y`
>>`tBodyAcc-std()-Z`
>>`tGravityAcc-mean()-X`
>>`tGravityAcc-mean()-Y`
>>`tGravityAcc-mean()-Z`
>>`tGravityAcc-std()-X`
>>`tGravityAcc-std()-Y`
>>`tGravityAcc-std()-Z`
>>`tBodyAccJerk-mean()-X`
>>`tBodyAccJerk-mean()-Y`
>>`tBodyAccJerk-mean()-Z`
>>`tBodyAccJerk-std()-X`
>>`tBodyAccJerk-std()-Y`
>>`tBodyAccJerk-std()-Z`
>>`tBodyGyro-mean()-X`
>>`tBodyGyro-mean()-Y`
>>`tBodyGyro-mean()-Z`
>>`tBodyGyro-std()-X`
>>`tBodyGyro-std()-Y`
>>`tBodyGyro-std()-Z`
>>`tBodyGyroJerk-mean()-X`
>>`tBodyGyroJerk-mean()-Y`
>>`tBodyGyroJerk-mean()-Z`
>>`tBodyGyroJerk-std()-X`
>>`tBodyGyroJerk-std()-Y`
>>`tBodyGyroJerk-std()-Z`
>>`tBodyAccMag-mean()`
>>`tBodyAccMag-std()`
>>`tGravityAccMag-mean()`
>>`tGravityAccMag-std()`
>>`tBodyAccJerkMag-mean()`
>>`tBodyAccJerkMag-std()`
>>`tBodyGyroMag-mean()`
>>`tBodyGyroMag-std()`
>>`tBodyGyroJerkMag-mean()`
>>`tBodyGyroJerkMag-std()`
>>`fBodyAcc-mean()-X`
>>`fBodyAcc-mean()-Y`
>>`fBodyAcc-mean()-Z`
>>`fBodyAcc-std()-X`
>>`fBodyAcc-std()-Y`
>>`fBodyAcc-std()-Z`
>>`fBodyAccJerk-mean()-X`
>>`fBodyAccJerk-mean()-Y`
>>`fBodyAccJerk-mean()-Z`
>>`fBodyAccJerk-std()-X`
>>`fBodyAccJerk-std()-Y`
>>`fBodyAccJerk-std()-Z`
>>`fBodyGyro-mean()-X`
>>`fBodyGyro-mean()-Y`
>>`fBodyGyro-mean()-Z`
>>`fBodyGyro-std()-X`
>>`fBodyGyro-std()-Y`
>>`fBodyGyro-std()-Z`
>>`fBodyAccMag-mean()`
>>`fBodyAccMag-std()`
>>`fBodyBodyAccJerkMag-mean()`
>>`fBodyBodyAccJerkMag-std()`
>>`fBodyBodyGyroMag-mean()`
>>`fBodyBodyGyroMag-std()`
>>`fBodyBodyGyroJerkMag-mean()`
>>`fBodyBodyGyroJerkMag-std()`

##References
[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012