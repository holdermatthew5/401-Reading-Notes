## Dunder Methods

Dunder methods don't just work with `__str__()` anything can replace 'str' to create a dunder method that does whatever you need it to.

## Probability

To calculate the probability of something happening, divide the number of times something can happen by all the other possibilities for each attempt.

## Intro to statistics

Statistical features is "probably" the most used statistics concept in datascience. It's usually the first stats technique applied.
Probability distribution is the percent chance that some event will occur.
Frequency stats applies math to analyze the probablity of some event occuring where. Only prior data is used.
Bayesian statistics does account for new data (like being told a die is rigged to only land on 6)

```
         P(B|A) P(A)
P(A|B) = -----------
             P(B)

- P(A|B) - Probability of A being true given that B is true.
- P(B|A) - Probability of B being true given that A is true.
- P(A) - Probability of A being true
- P(B) - Probability of B being true

from sklearn.naive_bayes import GaussianNB
from sklearn.metrics import accuracy_score

# Pick relevant features for dataset (x), the label is the credit score (y)
x = data1.loc[:,['loan_amnt', 'funded_amnt', 'funded_amnt_inv', 'int_rate']]
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.25,random_state=42)

# Create a Naive Bayes classifier
model_naive = GaussianNB()
model_naive.fit(x_train,y_train)
y_pred_naive_grade = model_naive.predict(x_test)
y_pred_naive_grade

# Calculate Accuracy of our Classifier
accuracy_score(y, y_pred_naive_grade)
```
