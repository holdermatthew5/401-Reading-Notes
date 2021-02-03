# Matplotlib

## Animation

I will be defining the input, output and purpose/action of the functions and methods from the 'Animation' section of the provided reading.

```
# New figure with white background
fig = plt.figure(figsize=(6,6), facecolor='white')
```

plt is the alias of the matplotlib module.
plt.figure instantiates the `Figure` ('Top level `Artist`, which holds all plot elements') and `SubplotParams` ('Controls the default spacing between subplots) classes.
There don't seem to be any sites talking about the inputs and output.

```
# New axis over the whole figure, no frame and a 1:1 aspect ratio
ax = fig.add_axes([0,0,1,1], frameon=False, aspect=1)
```

fig.add_axes() is a method that takes *args and **kwargs as arguments and adds an axis to fig.
  - rect - is a list with the size of the [left, bottom, width, height] as values in that order.
  - projection - is the projection type of the axis.
  - sharex, sharey - these parameters share the x/y axis with sharex and or sharey.
  - label - This parameter is the label for the returned axis.

```
# Number of ring
n = 50
size_min = 50
size_max = 50*50

# Ring position
P = np.random.uniform(0,1,(n,2))
```

np is the industry standard alias of numpy
np.random is a submodule within numpy. it's useful in cases where you might need random numbers.
np.random.uniform(low, high, size) takes in upper and lower limits and returns a single piece of data or a set of data depending on the size argument (can be int or tuple of ints for multiple draws and is an optional parameter).

```
# Ring colors
C = np.ones((n,4)) * (0,0,0,1)
# Alpha color channel goes from 0 (transparent) to 1 (opaque)
C[:,3] = np.linspace(0,1,n)
```

np.ones takes in a tuple with x, y and z parameters and returns a grid with the length of the x-axis being x, the length of the y-axis being y and the length of the z-axis being z. I would assume multiplying the calling of the function with only x and y arguments would be another way of adding the z-axis.
np.linspace(start, stop, num, endpoint, retstep, dtype, axis) returns a given number (num argument) of samples ranging in size from the start argument to the stop argument with a step argument only including every nth sample. the dtype argument can determine the datatype of the output or infers type of output from start and stop (when infering uses floats instead of ints). when the endpoint argument is set to False the stop argument is ignored. I don't understand what axis does.

```
# Ring sizes
S = np.linspace(size_min, size_max, n)

# Scatter plot
scat = ax.scatter(P[:,0], P[:,1], s=S, lw = 0.5,
                  edgecolors = C, facecolors='None')
```

.scatter uses its 12+ inputs to create and return a scatter plot.

```
# Ensure limits are [0,1] and remove ticks
ax.set_xlim(0,1), ax.set_xticks([])
ax.set_ylim(0,1), ax.set_yticks([])
```

.set_xlim and .set_ylim set the x and y limits of the scatter plot.
.set_xticks and .set_yticks sets the datas ticks for x and y axis.

```
def update(frame):
    global P, C, S

    # Every ring is made more transparent
    C[:,3] = np.maximum(0, C[:,3] - 1.0/n)

    # Each ring is made larger
    S += (size_max - size_min) / n

    # Reset ring specific ring (relative to frame number)
    i = frame % 50
    P[i] = np.random.uniform(0,1,2)
    S[i] = size_min
    C[i,3] = 1

    # Update scatter object
    scat.set_edgecolors(C)
    scat.set_sizes(S)
    scat.set_offsets(P)

    # Return the modified object
    return scat,
```

.maximum takes 2 arrays of ints and returns 1 array with the highest value of each index ([1,7,4] + [2,6,3] = [1,7,4]).
I can't find these 3
.set_edgecolors
.set_sizes
.set_offsets

```
animation = FuncAnimation(fig, update, interval=10, blit=True, frames=200)
# animation.save('rain.gif', writer='imagemagick', fps=30, dpi=40)
plt.show()
```

FuncAnimation makes an animation by repeatedly calling a function
I cant find the .save documentation but it looks like just saves frames of the animation.