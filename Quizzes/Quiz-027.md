# Tasks
A. Create a errorbar graph for the data below. You will need to calculate the mean and standard deviation first.

sensorA = [16, 24, 24, 9, 23, 26, 26, 23, 25, 14]  
sensorB = [2, 19, 25, 10, 11, 24, 17, 7, 24, 17]  
sensorC = [15, 11, 24, 21, 6, 2, 18, 27, 1, 16]  

B. Convert the following rgb color to hex color red=250, green=100, blue=10.



## Part A

### Code:

```.py
import matplotlib.pyplot as plt
import numpy as np
plt.style.use('dark_background')

sensorA = [16,24,24,9,23,26,26,23,25,14]
sensorB = [2,19,25,10,11,24,17,7,24,17]
sensorC = [15,11,24,21,6,2,18,27,1,16]

samples = []
for i in range(len(sensorA)):
    samples.append(i)

fig = plt.figure(figsize=(8,4))
plt.subplot(1,2,1)

plt.plot(samples,sensorA)
plt.plot(samples,sensorB)
plt.plot(samples,sensorC)

mean = []
standard_dev = []
max_v = []
min_v = []
for i in range(len(sensorA)):
    data = [sensorA[i],sensorB[i],sensorC[i]]
    mean.append(np.mean(data))
    standard_dev.append(np.std(data))
    max_v.append(max(data))
    min_v.append(min(data))

print(mean)
print(standard_dev)
print(max_v)
print(min_v)
print(samples)

plt.subplot(1,2,2)
plt.fill_between(samples,max_v,min_v,alpha=.5,linewidth=0,color="#55868C")
plt.errorbar(samples,mean,standard_dev,fmt="o")
plt.show()
```
