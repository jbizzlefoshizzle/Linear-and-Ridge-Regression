# Linear and Ridge Regression

The purpose of this project was to analyze and predict housing prices using attributes or features such as square footage, number of bedrooms, number of floors, and so on.

After a successful import of the data into a Jupyter Notebook, it is nice to see what types of data we are going to analyze and aggregate.
![dtypes]()
When cleaning up the data, I found it helpful to drop certain columns, in order to provide a cleaner dataframe.
![drop]()
Upon further inspection of the dataframe, I found that missing (or NaN) values existed for a few bedroom and bathroom entries. For this exercise, I decided that replacing the missing values with the mean values of the numbers of bedrooms and bathrooms, respectively, would aid in our analysis.
![replace]()
While the notebook itself includes some visualizations from the seaborn library, I found it helpful to look at what features had a strong correlation to the price.
![corr]()
To better understand correlation, I fit a linear regression model to predict house price using a feature like longitude coordinates,
![long]()
which predictably had a low R^2 value,
and a feature like square feet of living space, which had a much higher R^2 value.
![sqft_living]()
