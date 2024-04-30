NATIONAL POPULATION AND HOUSING CENSUS 2014

1.1 INTRODUCTION
Location and Size
Uganda is located in East Africa and lies across the equator, about 800 kilometres inland from
the Indian Ocean. It lies between 10 29ʼ South and 40 12ʼ North latitude, 290 34 East and 350
0ʼ East longitude. The country is landlocked, bordered by Kenya in the East; South Sudan in the
North; Democratic Republic of Congo in the West; Tanzania in the South; and Rwanda in South
West. It has a total area of 241,551 square kilometres, of which the land area covers 200,523
square kilometres. Administration
The country is divided into 111 districts and one City. The districts are further subdivided into
Counties, Sub counties and Parishes. The role of these local governments is to implement and
monitor government programmes at the respective levels. Overtime, the administrative units have
been sub-divided with the aim of easing administration and improving the delivery of services. The numbers of administrative units on the various census nights since 1969 are given in Table
1.1. Level of Administrative Unit
1969 1980 1991 2002 2014
District 21 33 38 56 112
County 111 140 163 163 181
Sub-county 594 668 884 958 1382
Parish 3,141 3,478 4636 5238 7241
Geography
Map of Uganda showing Districts and Urban Centres as of March 2014
1.2 DATASET
Importance
Information about the countryʼs population size, growth and distribution are critical
statistics that enable governments to make informed decisions, effectively plan and
monitor development progress. A good understanding of population trends and distribution
is essential in assessing future developments and service delivery. Population Census Dataset 1969-2014 has been used in this project. Data analysis
This dataset, containing 6 columns and 135 rows, was examined for its structure and
completeness, revealing no missing values during our data analysis
Population growth in Uganda from 1969-2014
Uganda had a total population of 3.4 million persons by 2014. Between August 1969 and
September 2014 period, the population of Uganda increased nearly five times from 5 million to
3.4 million (see Figure 2.1). Over a period of about 10 years (January 2002 to September 2014),
there was a net increase of 7.7 million persons in Uganda. This is the highest inter-censual
increase ever registered in Uganda. NOTE: The row (Uganda) is not a district its self as it portrays the summations of population of
districts in a particular year (Total Population)
Top 10 highly populated districts.
From this fig below, we see that between 1969-2014, the most highly populated district
in Uganda was Wakiso followed by Kampala. This enables the government to plan
accordingly for the resources when distributing them to different district. For example,
finance budgets
Algorithms
Algorithms implemented were two: Linear regression and Polynomial algorithms. These
were used to predict the population of people in a district for any year. Linear regres ion
Linear regression is a statistical method used to model the relationship between a
dependent variable and one or more independent variables by fitting a linear equation to
observed data. In simpler terms, it helps us understand how the value of one variable
changes with respect to another variable or variables. We designed an interface that enables the user to input the district from the list of
districts in Uganda and the year they need to predict. Then the predicted number of
people from that district are printed out
 From the dataset;  Independent variable (x): Year (as predictor variable).  Dependent variable (y): Population count (as the variable we want to predict).  Model Training:
From the scikit-learn library, the model is trained and fitted using the regression
class , for the fact that we were dealing with continuous feature and labels.  Prediction:
The prediction function takes the trained model and a year as input. It uses the coefficients and intercept learned during training to predict the population
for the given year using the formula of a straight line: y = mx + c, where m is the
coefficient and c is the intercept. The predicted population for the specified year is then printed out.  Evaluation Metrics
We have evaluated our models with one of cross validation techniques called
Leave one out Cross Validation (LOOCV).
This is due to the fact that for every district prediction the data set narrows
down to a few rows (about 5) an two columns (year and population) as shown
 Limitations
As most of the district growth is polynomial in nature it gives much bias in the predictions
according to the evaluation technique used
Polynomial Regres ion
Polynomial regression is a form of linear regression in which the relationship between the
independent variable(s) and the dependent variable is modelled as an nth degree
polynomial. It is used to predict the population of a specific district in Uganda for a
future year.  Here is how itʼs be n used.  The Dataset is transformed using the melt function to reshape it into a suitable
format, with columns for district, year, and population.  The degree of the polynomial regression model is set to 2 and polynomial
features are created from “Polynomial Features from sklearn. preproces ing.”  Model Training and Prediction
 The data is filtered to include only the population data for the specified district.  Leave One Out cross-validation is performed to evaluate the model's performance.  For each iteration:  The data is split into training and one sample testing sets.  Polynomial features are created for the training and testing sets.  The polynomial regression model is trained on the training data.  The population is predicted for the specified future year using the trained
model.  The Mean Squared Error (MSE) is calculated for the iteration.  The historical population data, polynomial trend line, and predicted
population for the future year are plotted on a scatter plot
 Results of Metrics:
1. Predicted Population: The algorithm predicts that the population of Uganda in the
year 2024 will be approximately over 45millions.
2. Mean Squared Error (MSE):  This gives a better bias compared to Linear Regression Model
 Limitations of the Polynomial Regres ion Algorithm:
Overfit ing: Polynomial regression models with higher degrees can easily overfit
the training data, capturing noise in the data rather than the underlying pattern. This can lead to poor generalization to unseen data, resulting in high MSE values
and unreliable predictions. Sensitivity to Model Complexity: The choice of the degree of the polynomial (in
this case, degree 2) can significantly impact the model's performance. Selecting
an inappropriate degree may lead to underfitting or overfitting, affecting the
accuracy of predictions. Conclusion
According to the analyzed data it shows that the increase in the mass number of
people in Uganda and most of its districts is exponential. And according to the created
polynomial model it predicts that the next census will have a mass of over 45million
Ugandans
