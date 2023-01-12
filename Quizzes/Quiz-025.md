# Tasks
A. Create a program shows the graph of the function below for 100 values of x in the interval -10 < x < 10.

B. Convert to decimal FFA5.

## Part A

### Code:

```.py
from matplotlib import pyplot as plt

def v_graph():
    x_ax = []
    y_ax = []
    st = -11
    for i in range(21):
        st += 1
        y = abs(st)
        x_ax.append(st)
        y_ax.append(y)
    return x_ax, y_ax

x_ax, y_ax = v_graph()
plt.plot(x_ax, y_ax)
plt.plot(x_ax, y_ax, color="teal")
plt.xlabel("x")
plt.ylabel("f(x) = |x|")
plt.show()
```
