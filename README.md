![suburb](./images/suburb.jpg)

# California Housing Price Predictor
The Repository explores predicting California housing prices in the 1990s using a `Linear Regression Model`. We use the `scikit` for the project and data required is available with scikit.

## Data

<div class="datatable">

|    Data Set Characteristics     |                 |
| ------------------------------- | --------------- |
| Number of instances             | 20640           |
| Number of attributes            | 8               |
| Attributes                      | <ul><li><em>MedInc</em> - median income in block group</li><li><em>HouseAge</em> - median house age in block group</li><li><em>AveRooms</em> - average number of rooms per household</li><li><em>AveBedrms</em> -  average number of bedrooms per household</li><li><em>Population</em> - block group population</li><li><em>AveOccup</em> - average number of household members</li><li><em>Latitude</em> - block group latitude</li><li><em>Longitude</em> - block group longitude</li></ul>          |
</div>

**Target** : `Median house value` - for California districts, expressed in hundreds of thousands of dollars ($100,000).

This dataset was obtained from the StatLib repository. https://www.dcc.fc.up.pt/~ltorgo/Regression/cal_housing.html

This dataset was derived from the 1990 U.S. census, using one row per census block group. A block group is the smallest geographical unit for which the U.S. Census Bureau publishes sample data (a block group typically has a population of 600 to 3,000 people).

A household is a group of people residing within a home. Since the average number of rooms and bedrooms in this dataset are provided per household, these columns may take surprisingly large values for block groups with few households and many empty houses, such as vacation resorts.

## Implementation Details 📜

- Standard [Linear Regression Model](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html) available with Scikit

- Input : Above data from the 1990s consensus

- Output : Median house price of the house in hundreds of thousands of dollars

### Steps 
1. Split the data into training and test dataset. We split it in the ratio of 80:20

2. Create a pipeline containing a StandardScaler and a LinearRegressionModel.

3. Fit the training data using the pipline to create the model.

4. Predict the results using the model ib the training data.

5. Compare the results to the given housing prices and calculate r2_score and Mean Squared error.


## Results
| Metric        | Value                        |
| ------------- | ---------------------------- |
| R2 Score      | 0.5891435539852219           |
| MSE           | 0.5472825858911409           |

The `R2 score` of 0.58 tells us that there is still lots of variability when comparing the model predicted results and the true values provided in the dataset. 

## Future Explorations
1. Evaluating whether to normalize Longitude and Latitude attributes of the dataset. Is there better way to represent the latitude and longitudes
2. Evaluating if we can add external data to improve the model and its accuracy
3. Evaluation of other feature engineering techniques to get better representative features.

## Libraries and Languages
**Language:** ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

**Packages:** ![sklearn](https://img.shields.io/badge/scikit-learn-orange)

## FAQs
#### What is Linear Regression ?
A linear regression model describes the relationship between a dependent variable, y, and one or more independent variables, X. Linear regression model is linear in terms of the coefficients. In this model, we try to fit a n-dimensional plane that represents the given data best.

For more details [MathWorks](https://in.mathworks.com/help/stats/what-is-linear-regression.html)


## Acknowledgements
- [scikit](https://scikit-learn.org/)
- [Linear regression @ MathWorks](https://in.mathworks.com/help/stats/what-is-linear-regression.html)
- [scikit-learn California Housing Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html#sklearn.datasets.fetch_california_housing)
- [123 of AI](https://123ofai.com/)
- [Suburb image by upklyak](https://www.freepik.com/free-vector/suburb-houses-suburban-street-with-cottages_9749999.htm#query=cartoon%20neighborhood&position=16&from_view=keyword&track=ais&uuid=8e41c6b6-8b91-4d3e-93d0-70e0f672fd20)

## Contact
If you have any feedback/are interested in collaborating, please reach out to me via [📧](mailto:raj.amal@gmail.com)


## License

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
