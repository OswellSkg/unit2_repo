# Tasks
A. Connect to the server and download the recordings data. From the data, build a linear model between t=610 and t=800.

## Part A

### Code:

```.py
import requests
import numpy as np
import matplotlib.pyplot as plt

readings = requests.get('http://192.168.6.142/readings').json()['readings'][0]

print(len(readings))

#get only temperature
temp=[]
for sample in readings:
    if sample['sensor_id']==4:
        temp.append(sample['value'])

#slice temperature to the region of interest
temp_afternoon_mon = temp[310:400]
x_afternoon_mon = []
for i in range(len(temp_afternoon_mon)):
    x_afternoon_mon.append(i)

plt.scatter(x_afternoon_mon,temp_afternoon_mon)

#linear model
m,b=np.polyfit(x_afternoon_mon,temp_afternoon_mon,1)
x_line = [10,len(temp_afternoon_mon)+10]
y_line = []
for i in x_line:
    y_line.append(m*(i)+b)

print(m,b)

plt.plot(x_line,y_line, 'black')
plt.show()
```


