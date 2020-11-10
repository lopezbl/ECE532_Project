# Updates

### 11/06/2020

Using [nasa_sort.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_sort.csv) and the [Least Squared.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Least%20Sqaured.ipynb), the least squared algorithm was used to see which features were the most important. Using all the features, the expected classification error is 9.39%. A method of ranking the features by their impact on the expected error was used. This technique concluded there were 7 features that allowed for a expected classification error of 9.34% which means the other features had little to no impact on the classification. The 7 features are "Absolute Magnitude", "Est Dia in KM(max)", "Orbit Uncertainty", "Minimum Orbit Intersection", "Semi Major Axis", and "Perihelion Distance".

Least Sqaured Data: [Least Squared.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Least%20Sqaured.ipynb)

### 11/02/2020

The [nasa.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa.csv) has been loaded and preprocessed. The [Load Data.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Load%20Data.ipynb) removes unnecessary columns such as ID numbers and dates of discovery/calculations and columns that have repeat information in different units/scales. This brought the number of features from 39 to 19. A [nasa_sort.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_sort.csv) was created for later use from the selected features. Using this csv, then the study of the three different algorithms can be conducted.

Original Data: [nasa.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa.csv)

Sorted Data: [nasa_sort.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_sort.csv)

Load Data Notebook: [Load Data.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Load%20Data.ipynb)

### 10/22/2020

Based on the [project description](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Description.pdf), a [project proposal](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Proposal.pdf) was made. The dataset chosen involves classifying if an asteroid is hazerdous or safe based on 39 features. As a result feature selection will be the main task.

Project Description: [Project Description.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Description.pdf)

Project Proposal: [Project Proposal.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Proposal.pdf)
