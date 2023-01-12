# Tasks
A. Compare the data from sensor#9 and 10 with smoothing of 12 samples.

B. What are the three main operators used in boolean logic?

## Part A

### Code:

```.py
import requests
import matplotlib.pyplot as plt

req = requests.get('http://192.168.6.142/readings')
data = req.json()
readings = data['readings'][0]

#get sensor 9
T9=[]
for sample in readings:
    if sample['sensor_id']==9:
        T9.append(sample['value'])

#get sensor 10
T10=[]
for sample in readings:
    if sample['sensor_id']==10:
        T10.append(sample['value'])


#y's
T9yaxis = []
T10yaxis = []
xaxis = []
for i in range(min(len(T9), len(T10))//12):
    s9 = 0
    s10 = 0
    for j in range(12):
        s9 += T9[i*12+j]
        s10 += T10[i*12+j]
    T9yaxis.append(s9/12)
    T10yaxis.append(s10/12)
    xaxis.append(12*i)

plt.subplot(2,1,1)
plt.plot(xaxis,T9yaxis)

plt.subplot(2,1,2)
plt.plot(xaxis,T10yaxis)

plt.show()
```

