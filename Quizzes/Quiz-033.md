# Tasks
A. Compare the data from sensor#6,8,9 and 10 by calculating and plotting the mean value for 500 samples.
#Plot the mean value for 500 samples for each sensor in a single plot.

## Part A

### Code:

```.py
import matplotlib.pyplot as plt
from matplotlib.gridspec import GridSpec

def get_sensor(id:int, url:str='http://192.168.6.142/readings') -> list:
    import requests
    req = requests.get(url)
    data = req.json()
    readings = data['readings'][4]
    sensor = []
    for r in readings:
        if r['sensor_id']==id:
            sensor.append(r['value'])
    return sensor

def smoothing(data:list, size_window:int=12)->list:
    x = [] #horizontal axis
    y = [] #smoothed version
    for i in range(0,len(data),size_window):
        segment_mean = sum(data[i:i+size_window])/size_window
        y.append(segment_mean)
        x.append(i)
    return x,y

sensors = [4,5]
values = []

for s in sensors:
    x,smoothed_value = smoothing(get_sensor(s)[:500])
    values.append(smoothed_value)

mean_per_hour = []
for i in range(len(values[0])):
    data = [values[n][i] for n in range(4)]
    mean_per_hour.append(sum(data)/len(sensors))

fig = plt.figure(figsize=(10,8))
gs = GridSpec(4,4,figure=fig)
#plot the mean of the sensors
ax = fig.add_subplot(gs[:,0:3]) #all the rows, column 0 and 1 and 2
plt.title("Mean of the sensors")
plt.plot(x,mean_per_hour,color="black")
plt.ylim([20,28])
plt.xlabel("Samples per hour")
plt.ylabel("Temperature(ºC)")

for row, color in [(0,"red"),(1,"blue"),(2,"green"),(3,"orange")]:
    ax = fig.add_subplot(gs[row,3]) #gs[row,column]
    plt.title(f"Sensor #{sensors[row]}")
    plt.plot(x,values[row],color=color)
    plt.ylim([15,28])
    plt.tick_params('x',labelbottom=False)

plt.tick_params('x',labelbottom=True)
plt.show()
```

