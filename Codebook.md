## ========================================================================
## Codebook Version 1.0
## For the tidy data from UCI HAR Dataset smart Phone Data        
## ========================================================================

### -------------------
### References
### -------------------


1. original data : https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
2. run_analysis.R : the R code used to create the tidy dataset : "subjectactivity.txt" or "subjectactivity.csv""
3. Readme.md : Explains the transforms used to create the tidy dataset
4. This file (Codebook.md ): Explains all key variables used in the transform and explains the variables in the tidy dataset "subjectactivity"

### -----------------------------------------------------------------------
### Transform variables used in run_analysis.R
### -----------------------------------------------------------------------

1. sTest : Dataframe holding the subject id's from test folder. Dimensions:  1 column and 2947 rows

2. xTest : Dataframe holding the X variables from test folder. Dimensions:  561 column and 2947 rows

3. yTest : Dataframe holding the activity type in numeric format. Dimensions:  1 column and 2947 rows

4. testAll : Combined test dataframe by merging subject, x, y and Names variables

5. sTrain : Dataframe holding the subject id's from train folder. Dimensions:  1 column and 7352 rows

6. xTrain : Dataframe holding the X variables from train folder. Dimensions:  561 column and 7352 rows

7. yTrain : Dataframe holding the activity type in numeric format. Dimensions:  1 column and 7352 rows

8. trainAll : Combined train dataframe by merging subject, x, y and Names variables

9. features : Dataframe names for names of x values read from features.txt 

10. xNames : Character vector with transposed names from features

11. allData : Combined test and train data rows and columns. Dimensions: 563 columns and 10299 rows

12. n1 to n7 : temporary variables used to standardize the labels in the combined dataset

13. p1 : temporary variables with all the indexes of 33 mean and 33 standard deviation measures and index for subject and activity type

14. subData : Subset of the allData with only mean and standard deviation measures and subject id and activity type

15. actMelt : Variable to id's(subject and activity. type) and measures(33 means and 33 standard deviations) to reshape the data

16. subjectData : re-shaped data using actMelt

17. subjectactivity.txt : output written using subjectData

### ---------------------------------------------------------------
### Variables in tidy Dataset : Subjectactivity.txt
### ---------------------------------------------------------------

1. subject : id of the each of the 30 participants in the study. file has one row per each subject. each row has the mean for each of the column item per subject
2. Columns 2 to 67 : All the means and standard deviations per subject when the subject was Laying down
3. Columns 68 to 135 : All the means and standard deviations per subject when the subject was Sitting
4. Columns 136 to 199 : All the means and standard deviations per subject when the subject was Standing
5. Columns 200 to 265 : All the means and standard deviations per subject when the subject was Walking
6. Columns 267 to 331 : All the means and standard deviations per subject when the subject was Walking Downstairs
7. Columns 332 to 397 : All the means and standard deviations per subject when the subject was Walking upstairs

### ---------------------------------------------------------------
###  End Notes
### ---------------------------------------------------------------

> _The transforms are explained in Readme.md_
>
> __The End__
