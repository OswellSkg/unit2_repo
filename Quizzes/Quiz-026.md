# Tasks
A. Create a program that ① show the graph and ②create a linear (H_model = m*h+b) for the data below:

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]

B. Convert the following color in hex to rgb #e6e627.


## Part A

### Code:

```.py
import matplotlib.pyplot as plt
import numpy as np

x = []
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]

for i in range(len(h)):
    x.append(i)


plt.plot(x, h, linestyle="none", marker="v")
#plt.scatter(samples, h, color="b", marker="v")
plt.title("Relative Humidity")
plt.ylabel("Relative Humidity (%)")
plt.xlabel("samples")

m,b = np.polyfit(x, h, 1)
print(f"Linear equation is y ={m:.2f}x+({b:.2f})")
x_model = [1, 33]
y_model = []
for i in x_model:
    y_model.append(m * i + b)
plt.plot(x_model, y_model, color = "teal")
plt.title("Humidity on Campus")

plt.show()
```
