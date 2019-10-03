Data&Variables 
=================

The variables forming this database correspond to columns or features of the orginal dataset downloaded from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

which contains the accelerometer and gyroscope 3_axial raw signals tAcc_XYZ(separated further into body and gravity acceleration signals (tBodyAcc_XYZ and tGravityAcc_XYZ)) and tGyro_XYZ. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk_XYZ and tBodyGyroJerk_XYZ). 

Also the magnitude of these three_dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc_XYZ, fBodyAccJerk_XYZ, fBodyGyro_XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. 

These signals were used to estimate variables of the feature vector for each pattern:  
'_XYZ' is used to denote 3_axial signals in the X, Y and Z directions.

tBodyAcc_XYZ
tGravityAcc_XYZ
tBodyAccJerk_XYZ
tBodyGyro_XYZ
tBodyGyroJerk_XYZ
tBodyAccMag
tGravityAccMag
tBodyAccJerkMag
tBodyGyroMag
tBodyGyroJerkMag
fBodyAcc_XYZ
fBodyAccJerk_XYZ
fBodyGyro_XYZ
fBodyAccMag
fBodyAccJerkMag
fBodyGyroMag
fBodyGyroJerkMag

The set of variables that were estimated from these signals are: 

mean: Mean value
std: Standard deviation
mad: Median absolute deviation 
max: Largest value in array
min: Smallest value in array
sma: Signal magnitude area
energy: Energy measure. Sum of the squares divided by the number of values. 
iqr: Interquartile range 
entropy: Signal entropy
arCoeff: Autorregresion coefficients with Burg order equal to 4
correlation: correlation coefficient between two signals
maxInds: index of the frequency component with largest magnitude
meanFreq: Weighted average of the frequency components to obtain a mean frequency
skewness: skewness of the frequency domain signal 
kurtosis: kurtosis of the frequency domain signal 
bandsEnergy: Energy of a frequency interval within the 64 bins of the FFT of each window.
angle: Angle between to vectors.

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle variable:

gravityMean
tBodyAccMean
tBodyAccJerkMean
tBodyGyroMean
tBodyGyroJerkMean 
=================

Data Manipulation
=================
After being downloaded, the files X_train,Y_train,subject_train were first merged into one single file,  assming that the order of rows in these files are precisely matched.

Then the same was performed to X_test,Y_test and subject_test. The resulting two files named as merged_train and merged_test were binded together.

The descriptive names were then applied to "Y" variable, using information contained in file activity_labels.txt. 

Variable or feature names representing data points of each column are modified from from file features.txt,relacing the special characters like "()" and "-". the final clean data set is named as HARUS_CLEAN_DT.csv.

A new file was created to calculate means of each variable for each activity and subject, the file was named as HARUS_AVG_DT.csv
