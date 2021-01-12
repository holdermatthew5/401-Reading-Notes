## Global Scope

- Changing a variable in a function only creates a second version for that function. When the function is finished the variable is reassigned the value it had prior to the function being called.
- Putting `global` before instantiating a variable will make it globally scoped. The variable does not have to exist outside the function before it's created globally in the function.
  - `number = 1` vs `global number = 1`
- As suspected, using global to modify scope is frowned upon and should be replaced with inserting the variable as an argument and assigning the returned value to the variable or by using `self.` to create an object property.
- If a function creating a global variable hasn't been run before the variable is referenced the program will crash with a NameError. To avoid this with `self.` remember to create the `self.` cariable in the `__init__` first.

## Nonlocal Scope

- If a function carries a variable and a nested function, the nested function can reference the variable, but cannot alter it. This can be changed by using nonlocal in the same manner as global.

```
def func():
    var = 100  # A nonlocal variable
    def nested():
        nonlocal var  # Declare var as nonlocal
        var += 100

    nested()
    print(var)

func()

TERMINAL: 200
```

^^^ [Copied from](https://realpython.com/python-scope-legb-rule/#the-global-statement)
- nonlocal can't be used outside of a local scope like a function or loop. It also cannot be used in a base function. It has to be in a nested function (or a loop in a function?).

```
first = 1
nonlocal first
second = 2
def second():
    nonlocal second
    third = 3
    def third():
        nonlocal third
```

^^^ When this code is run in its entirety the only variable that won't cause an error is third.
- nonlocal can't be used to create the first instance of a variable. It can only modify previously existing variables to be used in the base function.