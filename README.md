# Updates

11/06/2020

Using nasa_sort.csv, the least squared algorithm was used to see which features were the most important. Using all the features, the expected classification error is 9.39%. A method of ranking the features by their impact on the expected error was used. This technique concluded there were 7 features that allowed for a expected classification error of 9.34% which means the other features had little to no impact on the classification. The 7 features are "Absolute Magnitude", "Est Dia in KM(max)", "Orbit Uncertainty", "Minimum Orbit Intersection", "Semi Major Axis", and "Perihelion Distance". The code used for this determine can be found under Least Squared.ipynb.

11/02/2020

The data file and the corresponding code to load the data has been uploaded. The Load Data.ipynb removes unnecessary columns such as ID numbers and dates of discovery/calculations and columns that have repeat information in different units/scales. This brought the number of features from 39 to 19. A new nasa_sort.csv was created for later use from the selected features. Using this csv, then the study of the three different algorithms can be conducted.
