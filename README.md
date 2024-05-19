# Licence 
License: *This dataset is licensed under a Creative Commons Attribution 4.0 International (CC BY 4.0) license. Provided by: Billur Barshan Kerem Altun DOI: 10.24432/C5C59F*

*This allows for the sharing and adaptation of the datasets for any purpose, provided that the appropriate credit is given.*

*URL: https://archive.ics.uci.edu/dataset/256/daily+and+sports+activities*

# Information

This is a University Project in which I have covered several cluster algorithms like KMeans, DBSCAN and OPTICS for cluster analyisis.
The task was to pretent that I work for a company with a real world dataset and where I want to find clusters, that can bring value to the company.
The cluster analysis doesn't have to be successful, by finding meaningful clusters. 

# Goal
The goal in this project was to find clusters within eight subjects in the activity 'running'.

# The data
The sensor data is stored in subdirectories. In the directory *data* are 19 directories with the activities a01, a02 ... a19. In each of those directories are eight subdirectories for each of the subjects p1, p2 ... p8. In each of those directories are the sensor files s01.txt, s02.txt ... s60.txt.

**Data structure:**
- *data*
  - *a01*
    - *p1*
    - *p2*
      - *s01.txt*
      - *s02.txt*
      - *...*
  - *a02*
    - *p1*
    - *p2*
      - *s01.txt*
      - *s02.txt*
      - *...*
    - *...* 
    - 
**Explaining the features:**
`subject`: All eight subjects p1, p2, ... p7, p8

`activity`: The 19 activities are: 
- sitting (A1), 
- standing (A2), 
- lying on back and on right side (A3 and A4), 
- ascending and descending stairs (A5 and A6), 
- standing in an elevator still (A7) 
- and moving around in an elevator (A8), 
- walking in a parking lot (A9), 
- walking on a treadmill with a speed of 4 km/h (in flat and 15 deg inclined positions) (A1
- 0 and A11),
- running on a treadmill with a speed of 8 km/h (A12), 
- exercising on a stepper (A13), 
- exercising on a cross trainer (A14), 
- cycling on an exercise bike in horizontal and vertical positions (A15 and A16),
- rowing (A17), 
- jumping (A18), 
- and playing basketball (A19)

`timestamp`: timestamp of the data which was calculated during the concatenation of the data. 

`T_xacc ... LL_zmag`: Columns 4-49 correspond to: 
- T_xacc,  T_yacc,  T_zacc,  T_xgyro, ...,  T_ymag,  T_zmag,

- RA_xacc, RA_yacc, RA_zacc, RA_xgyro, ..., RA_ymag, RA_zmag,

- LA_xacc, LA_yacc, LA_zacc, LA_xgyro, ..., LA_ymag, LA_zmag,

- RL_xacc, RL_yacc, RL_zacc, RL_xgyro, ..., RL_ymag, RL_zmag,

- LL_xacc, LL_yacc, LL_zacc, LL_xgyro, ..., LL_ymag, LL_zmag

5 units on torso (T), right arm (RA), left arm (LA), right leg (RL), left leg (LL) and 9 sensors on each unit (x,y,z accelerometers, x,y,z gyroscopes, x,y,z magnetometers)


Therefore:

columns  4-12  correspond to the sensors in unit 1 (T), 

columns 13-22 correspond to the sensors in unit 2 (RA), 

columns 23-32 correspond to the sensors in unit 3 (LA), 

columns 33-42 correspond to the sensors in unit 4 (RL), 

columns 43-48 correspond to the sensors in unit 5 (LL).


First we have to iterate over all directories and concatenate all of those *.txt* files into one data_all.csv file. This is done with <code>pd.concat()</code>. This process is done in a separate jupyter file ***collect_data.ipynb*** and stored the data in **data_all.csv**. 

# File: experiments.ipynb
In this file I have done the cluster analysis

# File collect_data.ipynb
This is the code how I merged all the data form the subfolders into one file.

