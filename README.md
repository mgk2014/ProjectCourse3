ProjectCourse3
==============
Repo contains the code and markdownns for the "Getting and Cleaning Data" course project.

The following files are included in this repo:

* run_analysis.R - includes the main code and help function that executes the script to read, process and tidy data 
* CodeBook.md - describes the variable names, data and the specific transformations performed to produce the output tidy data set 
* README.md - this file, that describes how to run this script

INSTRUCTIONS TO INSTALL THE SCRIPT
==================================
Download the run_analysis.R script 

* Before running the script ensure that the Samsung wearable computing test data has been downloaded and unzipped on your computer. These datasets is available at
    * https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
    * description of data - http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 
* Once data has been unzipped, source the run_analysis.R script into R or RStudio from the location it was downloaded to
* set the working directory to the location of the data set. The script expects the working directory to be leading upto "UCI HAR Dataset". Please refer to example in the test() that is included in the run_analysis.R file
* if the script does not find all the source files in this data set, it will abort. please refer to the description link provided above for an understanding of the data set
* the output is written to the same folder level as "UCI HAR Dataset" into a folder called the "output" with the file name "project_course3_tidydata.txt"
* Common Error situations:
    Missing files: all files not present, data-set incomplete or files mis-named
    File structure errors: files are expected to be a certain structure, and rows. Number of rows in 
        X_train == subject_train == y_train. If the number of rows differs across these files, the script will not work.
        Same is true for the test data set
        features.txt - assumed that the no of features is same as the number of columsn in the X_train and X_test data-sets
*Memory - this scripts loads about 30Mb of data. Please ensure that the memory resources are available on the computer where this is run
    
SCRIPT LOGIC
============

The script proceeds in the following order, per the instructions of this course project
*   The script verifies if all the necessary files exist in the data-set in the current working directory. If any file is missing the script aborts.
*   The script reads feature names, selects the mean/std (removes the meanFreq) columns and cleans the names by convering all names to lower case, removing -,(,) symbols. The feature selection reduces the number of data columns in the data set from 561 to 66
*   The script then reads training data, subsets to columns of interest and binds subject and features columns. Script reads test data, subsets to columns of interest and binds subject and features columns. Script then combines the train and test data into one data frame. At the end of this step, the script contains 180 rows, 68 columns (66 for data, 2 for subject, activity)
*   The means of the data columns are calculated using the aggregate function grouped by subject, activity
*   The script replaces activity numbers with activity names, using factors
*   The final data-frame is written out to the output file