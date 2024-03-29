
# Activity Recognition Project
This folder contains following files realted to Activity Recognition Project
- Project report: ASU CSE 572 Data Mining - Porfolio Report.pdf
- Code: Project1.py, project1.ipynb


For code in Project.py
- Need following libraries - os, glob, numpy, pandas, matplotlib, sklearn
- All three section are well commented with relevant details


In this project, developed a computing system that can understand human activities, specifically eating action mixed with other unknown activities. The aim of this project is to identify the eating activities amongst the noise. And for this, I was provided with real world wristband data for a given activity.

In the first phase, I have done data cleaning, noise reduction, data organization and feature extraction.

## Phase 1: Data Cleaning and Organization

The data provided is collected using two sources:
1. Wristband data: Where the subject is wearing the wristband and performing eating actions periodically interspersed with non-eating unknown actions. The wristband provides you with i) accelerometer, ii) gyroscope, iii) orientation, and iv) EMG sensors. The sampling rate is 50 Hz for all the sensors.
2. Video recording of the person performing eating actions only used for establishing ground truth. In the data, you will be provided with the ground truth in the form of frame numbers where an eating action starts and ends. The actual video data will not be provided for privacy issues. The video data is taken at 30 frames per second. Hence you have to convert the frame numbers into sample numbers for the wristband sensors through some logic that you have to develop.The assumption that you can take is that the start frame and sample #1 of the wristband are synchronized. The output of this step will be a set of data snippetsthat are labelled eating actions and a set of data snippets that are non-eating.The way to convert the frame numbers into sample numbers is as follows:Consider the ground truth file, where there are three columns. Ignore the last column. The first column is the start frame of an eating action, the second column is the end frame. Each row is an eating action. The first frame number can be
multiplied by 50 and divided by 30. This gives you the corresponding sample number that indicates the start of an eating action. The second frame number can also be multiplied by 50 divided by 30 to get the end sample of an eating action. Do this for every row to get the sample numbers for eating actions for a person.

## Phase 2: Feature Extraction
In this task, need to select and implement five existing feature extraction methods such as Fast Fourier Transform, Discrete Wavelet Transform, a set of statistical features (min, max, avg, std, RMS, energy function), etc. The five types of feature extraction methods can be chosen by you. The aim is to use features that show clear distinction between the actions. A potential way of figuring out features is to plot the raw data, and try to visually understand differences. 

## Phase 3: Feature Extraction
This step involves reduction of the feature space and keeping only those features which show maximum distance between the two classes (eating and non-eating). Here are the steps
1. Arranging the feature matrix
2. Execution of PCA
3. Make sense of the PCA eigen vectors
4. Results of PCA

## Phase 4: User Dependent Analysis
In this phase, data split is done at user level and applied various classification models on it to check the performance.

## Phase 5: User Independent Analysis
In this phase, data split is done on overall data and applied various classificaiton models on it to check the performece.
