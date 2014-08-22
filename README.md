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

To `run_analysis.R` sript:
 * Loads and merges the training and the test sets to create a single data set.
 * Replaces the activity codes in the Samsung data with the corresponding activity names.
 * Labels the variables with descriptive variable names which match the names of the feature vectore form the Samsung data.
 * Extracts only the mean and standard deviation for each measurement form the feature vector. Measurments in the feature vector without a mean or standard deviation are discarded. 
 * Generates a second, independent tidy data set with the average of each variable by activity and subject and writes this data set to `course_project_tidyData.txt`.

The script itself also contains detailed comments. To **run the script**, it should be executed from the same directory that contains the `README.txt` of the Samsung data set.

## Codebook

For a description of variables, see the codebook.md file.


##References
[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012