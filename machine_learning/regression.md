# Regression

y = E[y|x] + measurement_error

y = f(x,beta)

- If dataset size(n) is small than parameter number(p) ( n < p ), hard to perform model
- If ( n == p ) and f is linear, model has unique solution.
- If n > p, set of beta value has to be found with minimizing distance dataset and predicted value ( ex. ordinary least squares )

## Linear Regression

$$ y = f(x,\beta) = \beta_0 + \beta_1 x_1 + error $$