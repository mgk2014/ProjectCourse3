ProjectCourse3
==============

Repo contains the code and markdownns for the "Getting and Cleaning Data" course project. 

The following files are included in this repo:

* run_analysis.R - includes the main code and help function that executes the script to read, process and tidy data

* CodeBook.md - describes the variable names, data and the specific transformations performed to produce the output tidy data set

* README.md - this file, that describes how to run this script

INSTRUCTIONS
============

* Download the run_analysis.R script 

* Before running the script ensure that the Samsung wearable computing test data has been downloaded and unzipped on your computer. These datasets is available at
    * https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
    * description of data - http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

* Once data has been unzipped, source the script into R, RStudio from the location it was downloaded to

* set the working directory to the location of the data set. The script expects the working directory to be leading upto "UCI HAR Dataset". Please refer to example in the test() that is included in the run_analysis.R file

* if the script does not find all the source files in this data set, it will abort. please refer to the description link provided above for an understanding of the data set

* the output is written to the same folder level as "UCI HAR Dataset" into a folder called the "output"

* Common Error situations:
    
    Missing files: all files not present, data-set incomplete or files mis-named
    
    File structure errors: files are expected to be a certain structure, and rows. Number of rows in 
        X_train == subject_train == y_train. If the number of rows differs across these files, the script will not work.
        Same is true for the test data set
        
        features.txt - assumed that the no of features is same as the number of columsn in the X_train and X_test data-sets
    
    Memory - this scripts loads about 30Mb of data. Please ensure that the memory resources are available on the computer where this is run
    
