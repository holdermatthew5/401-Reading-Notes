## Pandas in 10

To create a pandas object (a data table) assign `pd.Series([1, 3, 5, np.nan, 6, 8])`. This will build the following table.
```
0 1.0
1 3.0
2 5.0
3 NaN
4 6.0
5 8.0
```
Something I learned on my own. np.nan Can't be read with pandas (it'll show in the table, but you can't reference it as a string or NaN or pd.nan).
The y-axis is called the index. Does this mean I can reference index with `df.index[i]`? Doubt it, but it would be cool.
The x-axis are columns, so df.columns prints a tuple carrying a list of all columns in the dataset and the datatype saved as a string to the variable 'dtype' (`dtype='object'`).
`df.to_numpy()` prints a list of lists where each list corresponds to a row and each value in the nested lists is the value at a specific column in that row as shown below.
```
df

                A         B         C         D
2013-01-01  0.469112 -0.282863 -1.509059 -1.135632
2013-01-02  1.212112 -0.173215  0.119209 -1.044236
2013-01-03 -0.861849 -2.104569 -0.494929  1.071804
2013-01-04  0.721555 -0.706771 -1.039575  0.271860
2013-01-05 -0.424972  0.567020  0.276232 -1.087401

df.to_numpy()

array([[ 0.4691, -0.2829, -1.5091, -1.1356],
       [ 1.2121, -0.1732,  0.1192, -1.0442],
       [-0.8618, -2.1046, -0.4949,  1.0718],
       [ 0.7216, -0.7068, -1.0396,  0.2719],
       [-0.425 ,  0.567 ,  0.2762, -1.0874],
       [-0.6737,  0.1136, -1.4784,  0.525 ]])
```
You can reference a column by name (`df['A']` returns column A and the y-axis labels) or a row/set of rows by name or index (`df[0:3]` returns the first 3 rows; `df['2013-01-01':'2013-01-03']` shows all rows between those dates as well as those dates themselves).
You can reference both axis with `df.loc[:, []]` where the colon sets a range of rows to grab and the list contains all columns to be grabbed.
```
df.loc["20130102":"20130104", ["A", "B"]]
(will return)
                   A         B
2013-01-02  1.212112 -0.173215
2013-01-03 -0.861849 -2.104569
2013-01-04  0.721555 -0.706771
```