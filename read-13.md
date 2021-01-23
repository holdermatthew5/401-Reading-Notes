# How to run linear regretion in Python Scikit-Learn

Some modules for linear regression in python are:
  - numpy
  - scipy
  - stats model
  - scikitlearn

`df = pd.DataFrame(boston.data)` can convert a dataset to a pandas dataset but what does it convert from?
`df.columns` references a list of all columns. assigning it a new value will replace the column namse with those in the new list.
Add a new column and assign each of its values at the same time with `df['new_row'] = list_of_data`.
`im.fit()` - fits a linear model.
`im.predict()` - predict y using the linear model with estimated coefficients.
`im.score()` - Returns the coefficient of determination (R^2). A measure of how well observed outcomes are replicated by the model, as the proportion of total variation of outcomes explained by the model.
`.coef_` - provides estimated coefficients.
`.intercept_` - provides estimated intercepts.
To train your model use random inputs instead of like examples.
Finding patterns in graphed data likely means you are missing something. It could be that you are missing a correlation between seemingly unrelated variables.