## What is Jupyter Lab

Can switch cells between code and markdown.
'Shift + enter' runs cells.
    - Does it run all cells or just the ones on screen?
    - If it's the ones on screen does it run them from top to bottom?
Number to the left is the execution order.
All running on the same kernel
    - What's a kernel?
Kernal is restartable by pushing zero twice in command mode.
    - How do I get into command mode?

## NumPy Tutorial: Data Analysis with Python

NumPy came from Numeric.
Almost every data analysis/machine learning package uses NumPy in some way.
New line == new row
```
import csv
with open('file.csv', 'r') as f:
    data = list(csv.reader(f, delimiter=';'))
```
- It seems this forms the data in 'file.csv' into a list of lists where each nested list is a new line in 'file.csv' and each value from a given line (which was seperated by semicolons for this one - hence the `delimiter=';'`) is at its own index in that lines nested list.
    