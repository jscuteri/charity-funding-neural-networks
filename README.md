# Neural Networks/Deep Learning for Charity Funding

**Background**

The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. They want to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, I have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:


EIN and NAME—Identification columns

APPLICATION_TYPE—Alphabet Soup application type

AFFILIATION—Affiliated sector of industry

CLASSIFICATION—Government organization classification

USE_CASE—Use case for funding

ORGANIZATION—Organization type

STATUS—Active status

INCOME_AMT—Income classification

SPECIAL_CONSIDERATIONS—Special consideration for application

ASK_AMT—Funding amount requested

IS_SUCCESSFUL—Was the money used effectively

**ANALYSIS**

**Preprocess the data**

Using Pandas and the Scikit-Learn’s StandardScaler(), I haved preprocessed the dataset in order to compile, train, and evaluate the neural network model later.

  - I read in the charity_data.csv to a Pandas DataFrame, and identified the following:

    - What variable(s) are considered the target(s) for the model?
    - What variable(s) are considered the feature(s) for the model?

  - Drop the EIN and NAME columns.

  - Determine the number of unique values for each column.

  - For those columns that have more than 10 unique values, determine the number of data points for each unique value.

  - Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, Other, and then check if the binning was successful.

  - Use pd.get_dummies() to encode categorical variables
 
![Screen Shot 2022-03-12 at 4 01 45 PM](https://user-images.githubusercontent.com/87212158/158034847-e4c44d8e-d7f9-4726-8f64-994660f5a5dc.png)

**Compile, Train, and Evaluate the Model**

Using TensorFlow, I designed a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. Once completed I compiled, trained, and evaluated the binary classification model to calculate the model’s loss and accuracy.

  - Continue using the jupter notebook where you’ve already performed the preprocessing steps from before.

  - Create a neural network model by assigning the number of input features and nodes for each layer using Tensorflow Keras.

  - Create the first hidden layer and choose an appropriate activation function.

  - If necessary, add a second hidden layer with an appropriate activation function.

  - Create an output layer with an appropriate activation function.

  - Check the structure of the model.

  - Compile and train the model.
 
 ![Screen Shot 2022-03-12 at 4 02 41 PM](https://user-images.githubusercontent.com/87212158/158034879-50ea16d1-2858-47f6-9fea-de67d712582f.png)

  - Create a callback that saves the model's weights every 5 epochs.

  - Evaluate the model using the test data to determine the loss and accuracy.

  - Save and export your results to an HDF5 file.
 ![Screen Shot 2022-03-12 at 4 03 02 PM](https://user-images.githubusercontent.com/87212158/158034885-b9dd9ed2-d227-404f-89fd-8667947c3896.png)
