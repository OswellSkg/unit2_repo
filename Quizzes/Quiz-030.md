# Tasks
A. Using the data in the learning Log (Item 21), create a graph with a smoothed version where the smoothing window is every 4 points.

B. When was the internet first created? Remember to add your sources.

## Part A

### Code:

```.py
import matplotlib.pyplot as plt

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
plt.style.use('dark_background')

x = []
for i in range(len(h)):
    x.append(i)

size_window = 4
h_smth = []
x_smth = []
for i in range(0,len(h),size_window):
    values = h[i:i+size_window]
    h_smth.append(sum(values)/size_window)
    x_smth.append(i)

plt.subplot(2,1,1)
plt.plot(x,h, 'o-')

plt.subplot(2,1,2)
plt.plot(x_smth,h_smth, 'o-')

plt.ylabel("relative humidity")
plt.xlabel("Samples")
plt.show()
```


