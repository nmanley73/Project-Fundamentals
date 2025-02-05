# Project-Fundamentals

# Wind speed vs Power Output Linear Regression

## Instructions
In this project you must perform and explain simple linear regression using Python on the powerproduction dataset available on Moodle. The goal is to accurately predict wind turbine power output from wind speed values using the data set as a basis. To enhance your submission, you might consider comparing simple linear regression to other types of regression on this data set.

## Introduction

The goal of the project is to display linear regression on a dataset provided. The dataset contains the real world data of wind speed versus Power output. The plot of the data shows there is a definite relationship between the two variables. This makes the drawing on a straight line throiugh linear regression very straightforward. In the project i hope to explain how the concepts of linear regression, discuss other regression models and compare them to linear regression, explain the regression in this project and analyse its accuracy.

## Technologies and Python libraries used
The following applications and Python libraries were used in the creation of this project:
- Jupyter
- Git hub
- Python
  - numpy
  - matplotlib
  - pandas

## Code

import of libraries to be used
```
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
import pandas as pd
````
make plot tidier and bigger
```
plt.style.use("ggplot")
plt.rcParams["figure.figsize"] = (20,10)
```
set x equal to input (speed variable) and y to output (power variable)
```
x = df.speed
y = df.power
```
use polyfit function to plot the line, plot x and y variables and the best fit line
```
coeffs = np.polyfit(x,y,1)
plt.plot(x, y, '.', label = "Data")
c=plt.plot(x, coeffs[0]*x+coeffs[1], '-', label = "Best fit")
```
add title, xlabel, ylabel to the plot
```
plt.title("Turbine Power vs Wind Speed")
plt.xlabel("Wind Speed (mph)")
plt.ylabel("Power Outage (watts)");
```
## Analysis of plot
The datapoints that define the wind speed and power output relationship start close to the origin of the plot where as expected a low wind speed produces little power output from the turbine. From about 10mph there is a surge in power output along the diagonal of the chart from bottom left to top right of the plot. The datapoints eventually level off as maximum power output of the turbine seems to have been reached. The datapoints drop abruptly possibly due to the turbine switching itself off in excessive wind conditions. There are some outliers in the data which do not conform to the overall trend of the plot. This may be due to a mechanicel failure with the turbine. The plot indicates that the wind speed variable and power outage variable are heavily correlated and have a defined relationship which enables the prediction of wind turbine power output from wind speed values. The outliers in the data ensures that the dataset doesn't fit a straight line that well. 

## References

[1]-Renewables-info.com: Is wind energy environmentally friendly source of energy?; http://www.renewables-info.com/energy_news_and_reports/is_wind_energy_environmentally_friendly_source_of_energy.html?jjj=1609686518280

[2]-Resilience: IEA: Wind and solar capacity will overtake both gas and coal globally by 2024; https://www.resilience.org/stories/2020-11-12/iea-wind-and-solar-capacity-will-overtake-both-gas-and-coal-globally-by-2024/

[3]-windpower.generatorguide: Wind Power Calculator; http://windpower.generatorguide.net/wind-speed-power.html

[4]-towards data science: What is a Linear Regression?; https://towardsdatascience.com/the-concepts-behind-linear-regression-and-its-implementation-ffbab5a4d65e

[5]-data36.com: Linear Regression in Python using numpy + polyfit (with code base); https://data36.com/linear-regression-in-python-numpy-polyfit/is

[6]-Deep AI: Ordinary Least Squares; https://deepai.org/machine-learning-glossary-and-terms/ordinary-least-squares

[7]-stackoverflow: How can I display an image from a file in Jupyter Notebook?; https://stackoverflow.com/questions/11854847/how-can-i-display-an-image-from-a-file-in-jupyter-notebook

[8]-Listendata: 15 TYPES OF REGRESSION IN DATA SCIENCE; https://www.listendata.com/2018/03/regression-analysis.html

[9]-Investopedia: Multicollinearity; https://www.investopedia.com/terms/m/multicollinearity.asp

[10]-Datascience: Difference between Ridge and Linear Regression; https://datascience.stackexchange.com/questions/69661/difference-between-ridge-and-linear-regression

[11]-towardsdatascience: 5 Types of Regression and their properties; https://towardsdatascience.com/5-types-of-regression-and-their-properties-c5e1fa12d55e#:~:text=5%20Types%20of%20Regression%20and%20their%20properties%201,Regression.%20...%205%20ElasticNet%20Regression.%20...%206%20Conclusion

[12]-Upgrad: Linear Regression Vs. Logistic Regression: Difference Between Linear Regression & Logistic Regression; https://www.upgrad.com/blog/linear-regression-vs-logistic-regression/#:~:text=Difference%20between%20linear%20and%20logistic%20regression%20%20,threshold%20valu%20...%20%203%20more%20rows%20
