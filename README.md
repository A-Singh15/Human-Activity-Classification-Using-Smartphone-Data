# ENGR 845 Project : Human Activity Classification Using Smartphone Data 
![Activities Model](https://github.com/A-Singh15/Mini-Project-ENGR-845/blob/main/img/raw%202.png)

## Introduction
The purpose of this assignment is to gain hands-on experience with the concepts taught in the ENGR 845 class, including human data processing, feature engineering, pattern classification, parameter tuning, and model performance evaluation.

## References
- Canvas -> Mini Project -> Reference Materials -> Collect Accelerometer Data from Smartphone (For Use in Matlab)
- Canvas -> Mini Project -> Reference Materials -> Adding Machine Learning to Signal Processing Application
- Canvas -> Mini Project -> Reference Materials -> EMG PR code 2.0
- Canvas -> Weekly Lecture Slides
- Professor Yuriah

## Project Organization
- The `img` folder contains all the screenshots for the required Mini Project.
- The `data` folder contains all the data for the required Mini Project.
- The file `ENGR_845_MiniProject_Guideline.mlx` has all the required scripts and code for the Mini Project.

## Data Collection
In this assignment, 3-axis acceleration data from an *Android 13 Samsung A51 5G* for at least three different classes of human activities are collected from five users. The motions are walking, running, dancing, and standing.

**Data Collection Procedure:**
1. **Placement of the Device:** The device is placed on the waist pocket of each participant to ensure consistency throughout the data collection process.
2. **Number of Trials:** At least two trials are collected for each activity, with each trial lasting at least 5 seconds, repeated for all users.
3. **Sampling Frequency:** The sampling frequency for data collection needs to be specified and maintained consistently.
4. **Experimental Procedure:** Each trial starts and ends after the predefined duration. Data from each trial is saved in CSV structured files based on each activity.
5. **Field Testing:** Data was logged meticulously during field testing, capturing variability across different users and activities.

## Dataset Preparation
In this assignment, the dataset is located in the `data` folder. For each activity class, there are 12 files stored in the folder. The dataset is partitioned into training and testing sets, stored in the `train` and `test` folders, respectively.

## Data Logging
During the project, detailed logs were maintained for each user's activity trials. These logs captured:
- User identification
- Activity type
- Trial duration
- Environmental conditions
- Device orientation

This structured logging ensured reproducibility and consistency across all experiments.

## Raw Data Visualization
Below is MATLAB code to plot some example trials for the activities:

```matlab
% MATLAB code for raw data visualization
% Based on the Example, code in this section to plot the raw data that was collected
% Load the acceleration data
data = readmatrix('Data/accel_data.csv');

% Assuming the data contains x, y, and z acceleration in three columns
x_accel = data(:, 1);
y_accel = data(:, 2);
z_accel = data(:, 3);

% Plot the x, y, and z acceleration data
figure;

% Plot x acceleration
subplot(3, 1, 1);
plot(x_accel);
title('X Acceleration');
xlabel('Time');
ylabel('Acceleration');

% Plot y acceleration
subplot(3, 1, 2);
plot(y_accel);
title('Y Acceleration');
xlabel('Time');
ylabel('Acceleration');

% Plot z acceleration
subplot(3, 1, 3);
plot(z_accel);
title('Z Acceleration');
xlabel('Time');
ylabel('Acceleration');
