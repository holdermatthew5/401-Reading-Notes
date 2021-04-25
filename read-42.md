# Generators
A generator is any function that can pause its operation and resume it after the next call. This is done by using yield in place of a return (usually in a loop of some sort).

A generator must be assigned to a variables with it's arguments passed in at the time of creation to be used (`generator = generator_function(values)`). Time of creation will refer to the time the generator is assigned to a variable. Time of definition will refer to the time the containing script is ran.

When a generator is called for the first time it will run it's processes until it gets to a yield. Here it will stop and return the yielded value.

When a generator is called again after the first time it will resume its processes until the next yield.

When a generator finds the end of it's function it will return a StopIteration error proclaiming that the specified generator is out of uses.

Passing the generator into the list function (`list(generator)`) returns a list with all the values of the yields.

To find individual values use the next function instead of the list function.