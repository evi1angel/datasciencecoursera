This code book summarizes the resulting data fields in tidy.txt.

Identifiers
subject - The ID of the test subject
activity - The type of activity performed when the corresponding measurements were taken
Measurements
tBodyAccMeanX
tBodyAccMeanY
tBodyAccMeanZ
tBodyAccStdX
tBodyAccStdY
tBodyAccStdZ
tGravityAccMeanX
tGravityAccMeanY
tGravityAccMeanZ
tGravityAccStdX
tGravityAccStdY
tGravityAccStdZ
tBodyAccJerkMeanX
tBodyAccJerkMeanY
tBodyAccJerkMeanZ
tBodyAccJerkStdX
tBodyAccJerkStdY
tBodyAccJerkStdZ
tBodyGyroMeanX
tBodyGyroMeanY
tBodyGyroMeanZ
tBodyGyroStdX
tBodyGyroStdY
tBodyGyroStdZ
tBodyGyroJerkMeanX
tBodyGyroJerkMeanY
tBodyGyroJerkMeanZ
tBodyGyroJerkStdX
tBodyGyroJerkStdY
tBodyGyroJerkStdZ
tBodyAccMagMean
tBodyAccMagStd
tGravityAccMagMean
tGravityAccMagStd
tBodyAccJerkMagMean
tBodyAccJerkMagStd
tBodyGyroMagMean
tBodyGyroMagStd
tBodyGyroJerkMagMean
tBodyGyroJerkMagStd
fBodyAccMeanX
fBodyAccMeanY
fBodyAccMeanZ
fBodyAccStdX
fBodyAccStdY
fBodyAccStdZ
fBodyAccMeanFreqX
fBodyAccMeanFreqY
fBodyAccMeanFreqZ
fBodyAccJerkMeanX
fBodyAccJerkMeanY
fBodyAccJerkMeanZ
fBodyAccJerkStdX
fBodyAccJerkStdY
fBodyAccJerkStdZ
fBodyAccJerkMeanFreqX
fBodyAccJerkMeanFreqY
fBodyAccJerkMeanFreqZ
fBodyGyroMeanX
fBodyGyroMeanY
fBodyGyroMeanZ
fBodyGyroStdX
fBodyGyroStdY
fBodyGyroStdZ
fBodyGyroMeanFreqX
fBodyGyroMeanFreqY
fBodyGyroMeanFreqZ
fBodyAccMagMean
fBodyAccMagStd
fBodyAccMagMeanFreq
fBodyBodyAccJerkMagMean
fBodyBodyAccJerkMagStd
fBodyBodyAccJerkMagMeanFreq
fBodyBodyGyroMagMean
fBodyBodyGyroMagStd
fBodyBodyGyroMagMeanFreq
fBodyBodyGyroJerkMagMean
fBodyBodyGyroJerkMagStd
fBodyBodyGyroJerkMagMeanFreq

Activity Labels
WALKING (value 1): subject was walking during the test
WALKING_UPSTAIRS (value 2): subject was walking up a staircase during the test
WALKING_DOWNSTAIRS (value 3): subject was walking down a staircase during the test
SITTING (value 4): subject was sitting during the test
STANDING (value 5): subject was standing during the test
LAYING (value 6): subject was laying down during the test


Variables and descriptions

subject	- ID the subject who performed the activity for each window sample. Its range is from 1 to 30.

activity - Activity name

featDomain - Time domain signal or frequency domain signal (Time or Freq)

featInstrument - Measuring instrument (Accelerometer or Gyroscope)

featAcceleration - Acceleration signal (Body or Gravity)

featVariable - Variable (Mean or SD)

featJerk - Jerk signal

featMagnitude - Magnitude of the signals calculated using the Euclidean norm

featAxis - 3-axial signals in the X, Y and Z directions (X, Y, or Z)

featCount - Count of data points used to compute average

featAverage - Average of each variable for each activity and each subject

Dataset structure
Classes 'data.table' and 'data.frame':	11880 obs. of  11 variables:
$ subject         : int  1 1 1 1 1 1 1 1 1 1 ...
$ activity        : Factor w/ 6 levels "LAYING","SITTING",..: 1 1 1 1 1 1 1 1 1 1 ...
$ featDomain      : Factor w/ 2 levels "Time","Freq": 1 1 1 1 1 1 1 1 1 1 ...
$ featAcceleration: Factor w/ 3 levels NA,"Body","Gravity": 1 1 1 1 1 1 1 1 1 1 ...
$ featInstrument  : Factor w/ 2 levels "Accelerometer",..: 2 2 2 2 2 2 2 2 2 2 ...
$ featJerk        : Factor w/ 2 levels NA,"Jerk": 1 1 1 1 1 1 1 1 2 2 ...
$ featMagnitude   : Factor w/ 2 levels NA,"Magnitude": 1 1 1 1 1 1 2 2 1 1 ...
$ featVariable    : Factor w/ 2 levels "Mean","SD": 1 1 1 2 2 2 1 2 1 1 ...
$ featAxis        : Factor w/ 4 levels NA,"X","Y","Z": 2 3 4 2 3 4 1 1 2 3 ...
$ count           : int  50 50 50 50 50 50 50 50 50 50 ...
$ average         : num  -0.0166 -0.0645 0.1487 -0.8735 -0.9511 ...
 - attr(*, "sorted")= chr  "subject" "activity" "featDomain" "featAcceleration" ...
 - attr(*, ".internal.selfref")=<externalptr> 
Summaries
subject                   activity    featDomain  featAcceleration
Min.   : 1.0   LAYING            :1980   Time:7200   NA     :4680    
1st Qu.: 8.0   SITTING           :1980   Freq:4680   Body   :5760    
Median :15.5   STANDING          :1980               Gravity:1440    
Mean   :15.5   WALKING           :1980                               
3rd Qu.:23.0   WALKING_DOWNSTAIRS:1980                               
Max.   :30.0   WALKING_UPSTAIRS  :1980                               
     featInstrument featJerk      featMagnitude  featVariable featAxis 
Accelerometer:7200   NA  :7200   NA       :8640   Mean:5940    NA:3240  
Gyroscope    :4680   Jerk:4680   Magnitude:3240   SD  :5940    X :2880  
                                                              Y :2880  
                                                              Z :2880                                                                   
                                                                       
   count         average       
Min.   :36.0   Min.   :-0.9977  
1st Qu.:49.0   1st Qu.:-0.9621  
Median :54.5   Median :-0.4699  
Mean   :57.2   Mean   :-0.4844  
3rd Qu.:63.2   3rd Qu.:-0.0784  
Max.   :95.0   Max.   : 0.9745
