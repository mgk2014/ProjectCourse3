CodeBook: Samsung Wearable Computing Tidy Data
https://github.com/mgk2014/ProjectCourse3
July 2014

The tidy data set has been derived from the Samsung Wearable Computing Test data available at UCI Machine Learning Repository at http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The tidy data set was created per the instructions provided in the readme.md and the Coursera Getting and Cleaning course project. The tidy data set creation script merged training and test data, selected mean, freq columns, aggregates means, and replaced the activity numbers with meaningful text.

There are total of 180 rows and 68 columns in this data-set reflecting aggregate means for 30 subjects, performing 6 activities, for 66 features.

The feature/variable names in the output file are as follows

Data Elements
=============

Field Name: subject
Type: I           
Length: 2         
Description: Subject for who data was recorded     
Valid Values: 1-30

Field Name: activity                  
Type: C           
Length: 15        
Description: Activity performed by the subject     
Valid Values: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING

Remaining 66 filed listed below are computed values of the following type

Field Name: featureName               
Type: N           
Length: 16        
Description: Computed mean of the tested feature   
Valid Values: -1 to +1

tBodyAccmeanX            
tBodyAccmeanY
tBodyAccmeanZ           
tBodyAccstdX             
tBodyAccstdY             
tBodyAccstdZ            
tGravityAccmeanX         
tGravityAccmeanY         
tGravityAccmeanZ        
tGravityAccstdX          
tGravityAccstdY          
tGravityAccstdZ         
tBodyAccJerkmeanX        
tBodyAccJerkmeanY        
tBodyAccJerkmeanZ       
tBodyAccJerkstdX         
tBodyAccJerkstdY         
tBodyAccJerkstdZ        
tBodyGyromeanX           
tBodyGyromeanY           
tBodyGyromeanZ          
tBodyGyrostdX            
tBodyGyrostdY            
tBodyGyrostdZ           
tBodyGyroJerkmeanX       
tBodyGyroJerkmeanY       
tBodyGyroJerkmeanZ      
tBodyGyroJerkstdX        
tBodyGyroJerkstdY        
tBodyGyroJerkstdZ       
tBodyAccMagmean          
tBodyAccMagstd           
tGravityAccMagmean      
tGravityAccMagstd        
tBodyAccJerkMagmean      
tBodyAccJerkMagstd      
tBodyGyroMagmean         
tBodyGyroMagstd          
tBodyGyroJerkMagmean    
tBodyGyroJerkMagstd      
fBodyAccmeanX            
fBodyAccmeanY           
fBodyAccstdZ             
fBodyAccJerkmeanX        
fBodyAccJerkmeanY       
fBodyAccmeanZ            
fBodyAccstdX             
fBodyAccstdY            
fBodyAccJerkmeanZ        
fBodyAccJerkstdX         
fBodyAccJerkstdY        
fBodyAccJerkstdZ         
fBodyGyromeanX           
fBodyGyromeanY          
fBodyGyromeanZ           
fBodyGyrostdX            
fBodyGyrostdY           
fBodyGyrostdZ            
fBodyAccMagmean          
fBodyAccMagstd          
fBodyBodyAccJerkMagmean  
fBodyBodyAccJerkMagstd   
fBodyBodyGyroMagmean    
fBodyBodyGyroMagstd      
fBodyBodyGyroJerkMagmean

fBodyBodyGyroJerkMagstd
