## Classes and Objects

Objects contents are created by classes.
To assign the class template to an object assign it being called to a variablelike shown below.

```
class Myclass:
    variable = "blah"

    def function(self):
        print("words")

myobject = MyClass()
```

So to create an object you have to create a constructor and ^^that is the syntax for that.
Dot notation works.

You can actually have things other than functions in the tests file. Use objects `@pytest.fixture` to hold variables in objects.

```
@pytest.fixture
def simple_file():
    return StringIO('\n'.join(['abc'.'def']))
```

looks more like a function returning a variable after being introduced by a special comment.