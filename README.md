# Neural_Network_Charity_Analysis

UT Bootcamp Module 19 Challenge

## Project Overview
Use neural networks and to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Data provided from Alphabet Soup is a collection of 34,000 organizations that have been previously funded over the past few years.

## Resources
Data Sources provided to analyze and minipulate included:
- Alphabet Soup Charity dataset (charity_data.csv)

Software utilized for this study included:
- Python 3.7.6
- Pandas
- Personal GitHub account

## Analysis and Workflow

### Deliverable 1: Preprocessing the Data for a Neural Network
Spcifically for this deliverable we did the following:

1. Read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:
2. What variable(s) are considered the target(s) for your model?
3. What variable(s) are considered the feature(s) for your model?
4. Drop the EIN and NAME columns.
5. Determine the number of unique values for each column.
6. For those columns that have more than 10 unique values, determine the number of data points for each unique value.
7. Create a density plot to determine the distribution of the column values.
8. Use the density plot to create a cutoff point to bin "rare" categorical variables together in a new column, Other, and then check if the binning was successful.
9. Generate a list of categorical variables.
10. Encode categorical variables using one-hot encoding, and place the variables in a new DataFrame.
11. Merge the one-hot encoding DataFrame with the original DataFrame, and drop the originals (see below).

![alt text](https://github.com/austin020269/Neural_Network_Charity_Analysis/blob/main/Deli1_1.PNG)

12. Split the preprocessed data into features and target arrays.
13. Split the preprocessed data into training and testing datasets.
14. Standardize numerical variables using Scikit-Learn’s StandardScaler class, then scale the data (see below).

![alt text](https://github.com/austin020269/Neural_Network_Charity_Analysis/blob/main/Deli1_2.PNG)

### Deliverable 2: Compile, Train, and Evaluate the Model
Specifically for this deliverable we did the following:

1. Continue using the AlphabetSoupCharity.ipynb file where you’ve already performed the preprocessing steps from Deliverable 1.
2. Create a neural network model by assigning the number of input features and nodes for each layer using Tensorflow Keras.
3. Create the first hidden layer and choose an appropriate activation function.
4. If necessary, add a second hidden layer with an appropriate activation function.
5. Create an output layer with an appropriate activation function.
6. Check the structure of the model.
7. Compile and train the model.
8. Create a callback that saves the model's weights every 5 epochs.
9. Evaluate the model using the test data to determine the loss and accuracy.
9. Save and export your results to an HDF5 file, and name it AlphabetSoupCharity.h5 (see below). 

![alt text](https://github.com/austin020269/Neural_Network_Charity_Analysis/blob/main/Deli2_1.PNG)

Code: https://github.com/austin020269/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb

### Deliverable 3: Optimize the Model
Specifically for this deliverable we did the following:

1. Create a new Jupyter Notebook file and name it AlphabetSoupCharity_Optimzation.ipynb. Import your dependencies, and read in the charity_data.csv to a Pandas DataFrame. 
2. Preprocess the dataset like you did in Deliverable 1, taking into account any modifications to optimize the model. 
3. Design a neural network model, taking into account any modifications that will optimize the model to achieve higher than 75% accuracy. 
4. Create a callback that saves the model's weights every 5 epochs. 
5. Save and export your results to an HDF5 file, and name it AlphabetSoupCharity_Optimization.h5 (see below).

![alt text](https://github.com/austin020269/Neural_Network_Charity_Analysis/blob/main/Deli3_1.PNG)

Code: https://github.com/austin020269/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimization.ipynb

### Deliverable 4: A Written Report on the Neural Network Model
## Results 

#### Data Preprocessing
The prepocessing steps of the chosen model wanted to address the following questions:
1. What variable(s) are considered the target(s) for your model?  I created a target variable as the "IS_SUCCESSFUL" column.
2. What variable(s) are considered to be the features for your model?  All columns other than the "EIN" and "NAME" were considered model features.
3. What variable(s) are neither targets nor features, and should be removed from the input data?  The "EIN" and "NAME" columns were removed because they did not offer any benefit to the model.

#### Compiling, Training, and Evaluating the Model
During this step we wanted to address the following questions:
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?  This was trial and error starting with 2 layers and 12 neurons in the first layer and 6 in the second layer.  Changing these numbers did not measurably effect the outcome of my accuracy score.  I used the relu function throughout all of my models because it does better with nonlinear data.
2. Were you able to achieve the target model performance?  I was not able to achieve the target model performance of 75% but only 72.3%
3. What steps did you take to try and increase model performance?  I changed the layer/neuron combination a number of times without any change to the overall accuracy score.

## Summary
I was unable to obtain the 75% accuracy target.  Options that could be changed and may yield a higher accuracy would be using a different activation function or using a different number of layer/neuron combinations.
