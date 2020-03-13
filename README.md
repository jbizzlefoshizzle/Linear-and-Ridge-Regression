# Linear and Ridge Regression

The purpose of this project was to analyze and predict housing prices using attributes or features such as square footage, number of bedrooms, number of floors, and so on.

After a successful import of the data into a Jupyter Notebook, it is nice to see what types of data we are going to analyze and aggregate.
![dtypes](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/dtypes.png)

When cleaning up the data, I found it helpful to drop certain columns, in order to provide a cleaner dataframe.
![drop](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/drop.png)

Upon further inspection of the dataframe, I found that missing (or NaN) values existed for a few bedroom and bathroom entries. For this exercise, I decided that replacing the missing values with the mean values of the numbers of bedrooms and bathrooms, respectively, would aid in our analysis.
![replace](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/replace.png)

While the notebook itself includes some visualizations from the seaborn library, I found it helpful to look at what features had a strong correlation to the price.
![corr](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/corr.png)

To better understand correlation, I fit a linear regression model to predict house price using a feature like longitude coordinates,
![long](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/long.png)

which predictably had a low R^2 value,
and a feature like square feet of living space, which had a much higher R^2 value.
![sqft_living](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/sqft_living.png)

I also practiced fitting the linear regression model to predict house price with multiple features!
![multiple_features](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/multiple_features.png)

With a list of tuples containing estimators and model constructors,
I was able to create a pipeline object,
fit the object with the multiple features,
then fit the model in order to calculate correlation.
![pipe](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/pipe.png)

Importing some models from sci-kit learn, I split the data into training and testing sets.
![train_test_split](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/test_train_split.png)

I then created and fit a Ridge regression object, setting its regularization parameter and calculated its R^2 value.
With a value of 0.64, I then attempted to improve accuracy by performing a second-order polynomial transform on both training and testing data.
After refitting the Ridge regression object, the recalculated R^2 value increased to 0.70.
![ridge](https://github.com/jbizzlefoshizzle/Linear-and-Ridge-Regression/blob/master/Images/ridge.png)
