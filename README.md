### In this repo I want to make my conspects about regressions



### Features
- Conspect about polynomial regression (this kata solution https://www.codewars.com/kata/591748b3f014a2593d0000d9 )








### How Each Element in Linear Regression Works

Linear regression is a method that models the relationship between an independent variable `x` and a dependent variable `y` using a linear equation of the form:


y = b_0 + b_1 * x



Where:
- `y` — predicted value (dependent variable),
- `x` — independent variable (the factor that influences `y`),
- `b_0` — intercept (the point where the line intersects the y-axis),
- `b_1` — slope coefficient (shows how `y` changes when `x` changes).

Now, let's look at each element of linear regression and its role.

### 1. **Independent Variable `x`**

This is the data we use to make predictions. It can be any quantity that influences the dependent variable `y`. Examples:
- House size (`x`) and its price (`y`),
- A person’s age (`x`) and their weight (`y`).

`x` is the input data that we observe or measure, and it’s used to predict `y`.

### 2. **Dependent Variable `y`**

This is the result we’re trying to predict based on `x`. For example, if `x` is the size of a house, `y` could be its price. The task of regression is to find the relationship between `x` and `y`, and use it to predict new values of `y` based on future values of `x`.

### 3. **Slope Coefficient `b_1`**

The coefficient `b_1` shows how much `y` changes when `x` changes. The formula is:



b_1 = Σ[(x_i - x̄)(y_i - ȳ)] / Σ[(x_i - x̄)^2]




- **Numerator**: `Σ[(x_i - x̄)(y_i - ȳ)]` — this is the covariance between `x` and `y`. It shows how `x` and `y` vary together. If the covariance is positive, it means that as `x` increases, `y` also tends to increase.
  
- **Denominator**: `Σ[(x_i - x̄)^2]` — this is the variance of `x`, which measures how much the values of `x` deviate from their mean. It normalizes the covariance, allowing us to get a coefficient that is proportional to the change in `y` with respect to `x`.

**Role**: `b_1` is the slope of the regression line. It defines how strongly `y` depends on `x`. A large value of `b_1` means a strong dependence of `y` on `x`.

### 4. **Intercept `b_0`**

The intercept `b_0` is the point where the regression line intersects the y-axis when `x = 0`. The formula is:



b_0 = ȳ - b_1 * x̄




- **Mean value `ȳ`** — this is the average of all observed values of `y`.
- **Mean value `x̄`** — this is the average of all observed values of `x`.

**Role**: `b_0` defines the starting point of the regression line. It is the value of `y` when `x` is zero. It is important for understanding the overall position of the line on the graph, but does not reflect how `y` changes relative to `x`.

### 5. **Error (residuals)**

The difference between the real values `y` and the predicted values `ŷ` is called the error (or residual):


Error = y_i - ŷ_i



The sum of the squared errors is minimized when constructing the regression line. Squaring the errors ensures that both positive and negative errors contribute to the total error equally.

**Role**: Errors show how well the model fits the data. The smaller the errors, the better the model. The method of least squares (used in linear regression) minimizes the sum of squared errors.

### 6. **Predicted Values `ŷ`**

Once we have found the coefficients `b_0` and `b_1`, we can use them to predict new values of `y` for any given `x` using the equation:


ŷ = b_0 + b_1 * x



**Role**: This equation allows us to predict values of `y` for new `x` values. We use the model for forecasting in new situations or on new data.

### Conclusion:

1. **Independent Variable `x`** — the data we use to make predictions.
2. **Dependent Variable `y`** — the value we are trying to predict.
3. **Slope Coefficient `b_1`** determines the strength and direction of the relationship between `x` and `y`.
4. **Intercept `b_0`** determines the starting point of the regression line.
5. **Error** shows the deviation between real and predicted values.
6. **Predicted Value `ŷ`** uses the found coefficients to compute new values of `y` based on `x`.

Thus, linear regression builds a straight line that best describes the relationship between the variables and is used for making predictions.










