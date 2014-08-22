### Getting and Cleaning Data Course Project

## Codebook

This section contains information on all the variables included in the output data set from the `run_analysis.R` script.

**activity**	(factor)  
>Label that indicates which of the 6 activities the subject was performing:  
>>WALKING  - walking   
    WALKING_UPSTAIRS  - walking up a set of stairs  
    WALKING_DOWNSTAIRS  - walking down a set of stairs  
    SITTING  - sitting  
    STANDING  - standing   
    LAYING  -  laying down

**subject**	(factor)  
>ID number indicating which subject the data was collected from.  
>>Ranges from 1 to 30

**All Other Variables** (numeric)  
>The dataset includes 66 other variables, **the values of these variabels are the MEAN (by subject and activity) of the identically named feature variables** in the orignal Samsung data set. These variables represent pre-processed measurements from the smartphone's accelerometer (`Acc` in the variable name) and Gyroscope (`Gyro`) along all 3 axis (`-X`, `-Y`, `-Z` suffixes). All raw data from the phone was **captured in standard gravity units `g`**. 
>
>Data from the acceleromater has further been split into acceleration due to Gravity (`GravityAcc`) and acceleration due to movement of the subject's body (`BodyAcc`). Jerk and magnitude signals were also calculated and included as `Jerk` and `Mag` in the variable name respectively. The `t` and `f` prefixes indicate time-domain vs. frequency domain signals.

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
