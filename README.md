# NeuralNetworks

## Goal
Build a machine learning model that will be able to predict the success of a venture paid by Alphabet soup. The model should be able to determine the future decisions of the company by identifying projects likely to be a success, thus eligible to receive any future funding from Alphabet Soup.

## Resources
- Data: [alphabetSoup csv](https://github.com/JasmeerSangha/NeuralNetworks/blob/master/charity_data.csv)
- Python 3 scikit library

## Summary

1. Import data.
2. Remove identification columns (EIN, Name) as they do not contain any useful information for our model. 
3. Bin low frequency instances of categorical data.
4. Encode categorical data.
5. Merge encoded data with original dataframe.
6. Remove target column from features.
7. Split data into training and testing sets
8. Scale data to nullify any bias within the data set.
9. Fit model.

## Analysis/Results
There were 4 different neural networks used to predict the outcome of successful ventures. 

Version 1 ran for 50 epochs and consisted of two hidden layers, with 10 and 5 nodes. This set up allowed for a total of 581 parameters as the input had 51 variables. This resulted in an accuracy of 0.726. Future versions aimed to improve the accuracy in various ways:

Version 2: running the model for 100 epochs allowing more time for the model to fit the data. This resulted in a virtually identical accuracy score (0.721)

Version 3: running the model with larger hidden layers, 25 and 10 nodes. By increasing the number of connection it may be possible to identify a more subtle trend within the data. Alas this also returned an accuracy of 0.732

Version 4: running the model with another hidden layer again allows for more connections and thus a higher likelihood to identify a relationship between the features and the target. Again an accuracy of 0.729 was returned

Finally a random forest was used in hopes the ensemble strategy would be able to find a relationship the neural netwrok could not. This method returned an accuracy of 0.712

Altering the different aspects of our model did not significantly improve the fit. In future, the following steps could be taken for potentially better results:
- filtering out more features
- obtaining more data
- apply other machine learning models
