# coursera-getting-and-cleaning-data
<H1>Getting & Cleaning Data Peer Assessment</H1>

See the "Assessment Directions" for the directions from the course.

<H2>Description </H2>
<H3>Downloading Data</H3>

The first thing I do in my solution is check to see if the zip file is downloaded and if not then I download it. I did this mostly to check for it my own use. If it is there I print a warning. I also print the file creation time regardless.

<H3>File Preparation</H3>

The second step for me was to load all the pertinent files. As the project states I have assumed that all files are in the structure they were in the zip file with the main directory being the working directory of my code. For this project I excluded the inertial signal files. I put the column names on each of the test and training set files. I then used cbind() to append the subject and activity identifiers.

Finally, I merged the two files together using rbind().


<H3>Extract Mean & Standard Deviation Measurements</H3>

I decided to keep those variables that had the word mean or std in them and were the main function. So I kept mean() or meanfreq(), but not something like anglezgravitymean would not show up because to me that wasn't the point of mean and std calculations.


<H3>Tidy Data Output</H3>

I used melt and dcast to trim the data down and then summarize. I then output the file as a csv with headers.


<H3>Assessment Directions</H3>

You should create one R script called run_analysis.R that does the following:

1. Merges the training and the test sets to create one data set. The first step in my procedure is to download the data. The process will check to see if the zip file exists and if so it will give the user a warning message. If not it will download the zip file.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

<H3>Background</H3>

Wearable Computing Article - http://www.insideactivitytracking.com/data-science-activity-tracking-and-the-battle-for-the-worlds-top-sports-brand/

<H3>Data</H3>

Data Set - https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
Data Origination - http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
Deliverables

1. Please upload a tidy data set according to the instructions in the project description. Please upload your data set as a separate file (do not cut and paste a dataset directly into the text box, as this may cause errors saving your submission).

2. Please submit a link to a Github repo with the code for performing your analysis. The code should have a file run_analysis.R in the main directory that can be run as long as the Samsung data is in your working directory. The output should be the tidy data set you submitted for part 1. You should include a README.md in the repo describing how the script works.
