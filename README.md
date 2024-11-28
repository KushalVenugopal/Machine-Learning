# Machine-Learning

Dabbling in some Machine Learning brought excitement and added extra challenge to my time at The University of Queensland - May 2022

The aim of this project was to:

- Create a Machine Learning pipeline
- Given a random dataset, analyse the dataset
- Extract details and insights fom said dataset

Another use of this project was to demostrate the working of some Machine Learning concepts.

Tools used were:

- Jupyter Notebook
- Python (numpy, pandas, scikit-learn, matplotlib)

The dataset used is attached.
The description of the project and the pipeline is given below.

1. Exploratory data analysis

2. Data pre-processing
   • Data Imputation
   • Data Scaling

3. Dimensionality Reduction – Principal Component Analysis
   • Scree graph – show how many components are ideal
   • Scree graph – show how much variance each component holds
   • Reducing to 2D visualize

4. Classification – Random Forest Classification
   • Introduction
   • Before doing PCA – verifying the accuracy
   • After doing PCA – verifying the accuracy
   • Effect of PCA on the accuracy of the classifier
   • Predicting the unknown categories

Exploratory Data Analysis:
The dataset seems to be categorized mainly into Desktop/Server/Laptop/Mobile categories. The dataset has 8 dimensions that contain continuous data.

Data Pre-Processing:
During pre-processing, we fill out missing values in our dataset and scale the data to make the data in each feature relative to each other.
Iterative Imputer:
IterativeImputer is a scikit-learn class that helps in filling out missing data in the dataset. It models features with missing values as functions of the rest of the features respectively. This fits a regressor on each feature, where the said feature column is treated as output and the rest of the feature columns as inputs.
So, the values filled out in place of the missing values are computed by regression, to be accurate.
One of the arguments we change in the iterative imputer is max_iter. The IterativeImputer will do the regression for each feature column max_iter number of times, and the output is the result at the end of the last iteration.

MinMax Scaler:
MinMaxScaler is a scikit-learn class that helps in scaling all the data in the given dataset.
The MinMaxScaler class scales the data in each column of the given dataset such that all of the data is scaled between 0 and 1. This helps in building accurate models.

Dimensionality Reduction:
Dimensionality reduction is a method used to reduce the number of dimensions of a dataset, in most cases to be able to visualize the given data.
If the number of dimensions is reduced, processing of the data or fitting a model to the data happens quicker.
Here we chose Principal Component Analysis (PCA), to reduce the number of dimensions of the data.
The plot below shows the number of components of the data vs how much of the variance those many components together hold.

Classification:
In the dataset, it can be observed that many values in the “category” column are labelled as ‘Unknown’.
We will use classification to try to predict into which category the unknown processors fall.
We separate the data set into known and unknown categories. We will train our classifier on a part of our known dataset, test it on a small part of our known dataset, and then predict the categories of the unknown dataset.
For the classification, we chose the Random Forest Classifier.
