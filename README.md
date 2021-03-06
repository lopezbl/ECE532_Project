# Updates

### 12/12/2020

The final report, [Final Report.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Final%20Report.pdf), has been submitted.

Final Report: [Final Report.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Final%20Report.pdf)

### 12/05/2020

The final testing notebook, [Final Testing.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Final%20Testing.ipynb), has been put together for the three algorithims. This summarizies the key results and reccomends the neural network for future classification uisng the "Absolute Magnitude" and "Minimum Orbit Intersection" as the only features. 

Final Testting Notebook: [Final Testing.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Final%20Testing.ipynb)

### 12/04/2020

In the earlier algorithms, it was discovered there were 2-3 features that created a visible boundary line for the two classes. However, LASSO and least squared were not capable of accurately creating the decision boundary with the few features. These algorithms had to make use of weakly correlated features in order to account for this. As a result, they did not generalize well. Two neural networks were trained to try to capture the decision boundary. First, a more automated neural network algorithm using Pytorch was used to study the impact of training the neural network on the oversampled data compared to the original data. This is outlined in [Neural Network Pytorch.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Neural%20Netwokr%20Pytorch.ipynb). It was found that using the original data and the oversampled data led to the same error. However, the neural network built on the oversampled had a higher accuracy on the hazardous class then the original data did. Considering the hazardous class is the more important to be highly accurate, the oversampling was used for parameter using the backpropagation code in [Neural Network Prop.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Neural%20Netwokr%20Prop.ipynb). 

The back propagation code in [Neural Network Prop.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Neural%20Netwokr%20Prop.ipynb), first determines the behaviour of the neural network for all features. This model led to low accuracy for the hazardous class as the uncorrelated features make training the neural network difficult. Then the three important features and two important features were used to train a neural network at the same parameters. It was determined from this that two feature model was just as good at predicting as the three feature model. As a result, the two feature model was then used to understand and improve the parameters for back propagation. First the number of hidden nodes and epochs were set to be proportional while keeping the learning rate constant. This determined that 10 hidden nodes were optimal. Then the number of hidden nodes and epochs was kept constant and the learning rate was varied. The learning rate was found to be best in the 0.1 to 0.3 range and 0.2 was chosen. The final neural network was then trained at for 10 hidden nodes and a learning rate of 0.2. This led to an overall error of just 0.9% and 0.9% for the hazardous class and 0.8% for the other when tested on the original data. 

The final neural network was then used to predict the test data. It had an overall error of just 0.2% with 0% for the hazardous class and 0.3% for the other. This means the neural network was able to accurately determine the decision boundary. 

Pytorch Neural Net: [Neural Network Pytorch.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Neural%20Netwokr%20Pytorch.ipynb)

Manual Neural Net: [Neural Network Prop.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Neural%20Netwokr%20Prop.ipynb)

### 12/01/2020

A project update was submitted with progess made thus far and a revised timeline for completion. 

Project Update 2: [Project Update 2.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Update%202.pdf)

### 11/28/2020

Final testing of the algorithms completed thus far was conducted using [Partial Testing.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Partial%20Testing.ipynb) and the testing data [nasa_test.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_test.csv). The base least squared case with seven features classified each asteroid as being non-hazardous with an error of 15.8%. This is not surprising considering the imbalance of the class types. The initial guess of three features for the least squared with SMOTE had a prediction accuracy of 13.4% but had an hazardous error of 27.0%. The results from the least squared ranking technique with SMOTE and five features had the same results as the case without SMOTE despite promising results on the training data. The LASSO algorithm with SMOTE has had the best results with six features giving an error of 19.6%. This error is higher, but the error for the hazardous class had an error of 0%. This means that if the classification says the asteroid is safe, then one can confidently assume it is safe. The neural network algorithm has to be fully completed so final testing and comparison will be made later. 

Partial Testting Notebook: [Partial Testing.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Partial%20Testing.ipynb)

### 11/24/2020

The LASSO algorithm with SMOTE has been completed using [LASSO SMOTE.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/LASSO%20SMOTE.ipynb) and the training data [nasa_train.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_train.csv). Each weight solved for in the notebook uses the ista_solve_hot function which takes an array of regularization parameters and returns weight for each regularization parameter. Then the regularization parameter with the lowest error on the pre over sampled data (before SMOTE is applied) is chosen. A ranking method was used in this algorithm as well. However, instead of deleting features, the feature with the lowest weight was deleted. This is possible because the original features, which are all positive, have been scaled to be between 0 and 1. This ranking method identified seven features of importance. However, during validation it was found one feature was not necessary. This makes results of this ranking method less trustworthy. The six features suggested by this algorithm are "Absolute Magnitude", "Minimum Orbit Intersection", "Jupiter Tisserand Invariant", "Orbital Period", "Perihelion Distance", and "Aphelion Dist". These features fina an overall error of 13.2% with an error of just 0.6% for the hazardous class. These results are the best thus far. 

LASSO with SMOTE Notebook: [LASSO SMOTE.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/LASSO%20SMOTE.ipynb)

### 11/17/2020

A project update was submitted with progess made thus far and a revised timeline for completion. 

Project Update 1: [Project Update 1.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Update%201.pdf)

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

Test Data: [nasa_test.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_test.csv)

Train Data: [nasa_train.csv](https://github.com/lopezbl/ECE532_Project/blob/main/nasa_train.csv)

Load Data Notebook: [Load Data.ipynb](https://github.com/lopezbl/ECE532_Project/blob/main/Load%20Data.ipynb)

### 10/22/2020

Based on the [project description](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Description.pdf), a [project proposal](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Proposal.pdf) was made. The dataset chosen involves classifying if an asteroid is hazerdous or safe based on 39 features. As a result feature selection will be the main task.

Project Description: [Project Description.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Description.pdf)

Project Proposal: [Project Proposal.pdf](https://github.com/lopezbl/ECE532_Project/blob/main/Project%20Proposal.pdf)
