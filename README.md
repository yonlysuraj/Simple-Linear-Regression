# Simple Linear Regression Project

## Analyzing Sales and Advertising Relationships

This project demonstrates a simple linear regression model to analyze the relationship between sales and advertising data for a dietary weight control product.

## Table of Contents

1. Overview 
2. License
3. Dependencies
4. Problem Definition
5. Implementation Details
6. Results and Analysis
7. Model Validation
8. References

## Overview

This project uses Python and scikit-learn to implement a simple linear regression model. We'll examine how advertising spending affects sales using statistical analysis and machine learning techniques.

## License

This project is licensed under Creative Commons Attribution 4.0 International.
- Share: Copy and redistribute in any medium
- Adapt: Remix, transform, and build upon the material

## Dependencies

Required Python libraries:
- NumPy: Numerical computing
- pandas: Data manipulation 
- scikit-learn: Machine learning
- matplotlib: Data visualization

## Problem Definition

We aim to:
1. Model the relationship between advertising spend and sales
2. Evaluate model performance using RMSE and R² metrics
3. Validate model assumptions and reliability

## Implementation Details

### The Linear Regression Model

The model follows the equation:
```
Y = β₀ + β₁X
```
Where:
- X: Independent variable (Advertising)
- Y: Dependent variable (Sales)
- β₀: Y-intercept
- β₁: Slope coefficient

![](Images/Scatter%20plot%20of%20X%20and%20y.png)

Now, our task is to find a line which best fits the above scatter plot. This line will help us to predict the value of any Target variable for any given Feature variable. This line is called regression line. 
We can define an error function for any line. Then, the regression line is the one which minimizes the error function. Such an error function is also called a Cost or a Cost function.

### Cost Function

We want the above line to resemble the dataset as closely as possible. In other words, we want the line to be as close to actual data points as possible. It can be achieved by minimizing the vertical distance between the actual data point and fitted line. We calculate the vertical distance between each data point and the line. This distance is called the residual. So, in a regression model, we try to minimize the residuals by finding the line of best fit.

![](Images/Diagrammatic%20Representation%20of%20Residuals.png)

We can try to minimize the sum of the residuals, but then a large positive residual would cancel out a large negative residual. For this reason, we minimize the sum of the squares of the residuals. 

Mathematically, we denote actual data points by yi and predicted data points by ŷi. So, the residual for a data point i would be given as 
				
       				
				di = yi -  ŷi
				

Sum of the squares of the residuals is given as:


				 D = Ʃ di2       for all data points

This is the Cost function. It denotes the total error present in the model which is the sum of the total errors of each individual data point. We can represent it diagrammatically as follows:-

![](Images/Ordinary%20Least%20Squares.png)

We can estimate the parameters of the model β₀ and β₁ by minimizing the error in the model by minimizing D. Thus, we can find the regression line given by the equation above. This method of finding the parameters of the model and thus regression line is called Ordinary Least Square Method.

### Model Performance 

Performance metrics used:
- RMSE (Root Mean Square Error): Measures prediction accuracy
- R² Score: Explains variance in the model

### Results

Key findings:
- RMSE: 11.23
- R² Score: 0.579 (57.9% variance explained)
- Model shows signs of underfitting

## Model Validation

### Assumptions Tested:
1. Linearity
2. Normal distribution
3. No multicollinearity
4. No autocorrelation
5. Homoscedasticity

![](Images/Residual%20errors.png)

If the data points in a residual plot are randomly dispersed around the horizontal axis and an approximate zero residual mean, a linear regression model may be appropriate for the data. Otherwise, a non-linear model may be more appropriate.

If we take a look at the generated ‘Residual errors’ plot, we can clearly see that the train data plot pattern is non-random. Same is the case with the test data plot pattern.
So, it suggests a better-fit for a non-linear model.

## References

The concepts and ideas in this project have been taken from the following websites and books:

- [Machine learning notes by Andrew Ng](https://www.coursera.org/learn/machine-learning)
- [Wikipedia: Linear regression](https://en.wikipedia.org/wiki/Linear_regression)
- [Wikipedia: Simple linear regression](https://en.wikipedia.org/wiki/Simple_linear_regression)
- [Wikipedia: Ordinary least squares](https://en.wikipedia.org/wiki/Ordinary_least_squares)
- [Wikipedia: Root-mean-square deviation](https://en.wikipedia.org/wiki/Root-mean-square_deviation)
- [Wikipedia: Coefficient of determination](https://en.wikipedia.org/wiki/Coefficient_of_determination)
- [Statistics Solutions: Assumptions of Linear Regression](https://www.statisticssolutions.com/assumptions-of-linear-regression/)
- Python Data Science Handbook by Jake VanderPlas
- Hands-On Machine Learning with Scikit Learn and Tensorflow by Aurilien Geron
- Introduction to Machine Learning with Python by Andreas C Muller and Sarah Guido


























