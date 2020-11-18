# Updates

### 11/16/2020

Using [nasa_train.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_train.csv) and the [Least Squared SMOTE.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Least%20Squared%20SMOTE.ipynb), the least squared algorithm along with SMOTE was used to see which features were the most important. Using all the features for training on the expanded data set and then evaluating on the original data, the classification error was 13.7%. This is higher than just using least squared, but the accuracy of the hazardous case improved. The same method of ranking the features by their impact on the expected error was used. This technique concluded there were 5 features that allowed for a classification error of 13.3% which means the other features had little to no impact on the classification. The 5 features are "Absolute Magnitude", "Minimum Orbit Intersection", "Semi Major Axis", "Perihelion Distance", and "Aphelion Dist". The confusion matrix shows an accuracy of 99.7% for the hazardous cases and 84.1% for the nonhazardous class. The use of SMOTE increased the overall error but balanced the accuracy of the models.


Least Sqaured with SMOTE Notebook: [Least Squared SMOTE.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Least%20Squared%20SMOTE.ipynb)

### 11/06/2020

Using [nasa_train.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_train.csv) and the [Least Squared.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Least%20Squared.ipynb), the least squared algorithm was used to see which features were the most important. Using all the features, the expected classification error is 9.46%. A method of ranking the features by their impact on the expected error was used. This technique concluded there were 7 features that allowed for a expected classification error of 9.34% which means the other features had little to no impact on the classification. The 7 features are "Absolute Magnitude", "Est Dia in KM(max)", "Orbit Uncertainty", "Minimum Orbit Intersection", "Semi Major Axis", "Perihelion Distance", and "Aphelion Dist". However, the confusion matrix shows an accuracy of about 50% for the hazardous cases. This can be explained by the difference in size between the two classes; the hazardous class is just 16% of the data. Based on this, a method called SMOTE will be used to increase the sample size of the hazardous class.

Least Sqaured Notebook: [Least Squared.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Least%20Squared.ipynb)

### 11/01/2020

The [nasa.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa.csv) has been loaded and preprocessed. The [Load Data.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Load%20Data.ipynb) removes unnecessary columns such as ID numbers and dates of discovery/calculations and columns that have repeat information in different units/scales. This brought the number of features from 39 to 19. A [nasa_filt.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_filt.csv) was created and has all of the data with the 19 features. From this, the [nasa_test.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_test.csv) was created from 10% of the data for final testing of the three algorithims. The remaining 90% of the data was places in [nasa_train.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_train.csv) for training of the three algorithims.

Original Data: [nasa.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa.csv)

Filtered Data: [nasa_filt.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_filt.csv)

Test Data = [nasa_test.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_test.csv)

Train Data = [nasa_train.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_train.csv)

Load Data Notebook: [Load Data.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Load%20Data.ipynb)

### 10/22/2020

Based on the [project description](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Description.pdf), a [project proposal](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Proposal.pdf) was made. The dataset chosen involves classifying if an asteroid is hazerdous or safe based on 39 features. As a result feature selection will be the main task.

Project Description: [Project Description.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Description.pdf)

Project Proposal: [Project Proposal.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Proposal.pdf)
