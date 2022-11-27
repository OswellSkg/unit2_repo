## 11.11.22 Quiz #024

Create a program shows the graph of the parabola for 100 values of x in the interval -10 < x < 10.
f(x) = 2(x+5)^2


------------------------------------------------------------------------

Program:
```.py
import matplotlib.pyplot as plt

def equation():
    x_list = []
    y_list = []
    for i in range(100):
        x = -10+i*0.2
        x_list.append(x)
        y = 2*(i+5)**2
        y_list.append(y)
    return y_list,x_list

data_y,data_x = equation()

plt.plot(data_x, data_y, color="r")
plt.xlabel("x")
plt.ylabel("$y=2(x+5)^2$")
plt.show()
```

------------------------------------------------------------------------

Proof:
### Fig.1
Input: x,y | Output: Graph
<img width="1656" alt="Screen Shot 2022-11-28 at 2 25 06" src="https://user-images.githubusercontent.com/112055140/204150424-12175918-bea9-445d-b80e-7294ee1eecaf.png">


------------------------------------------------------------------------

### Circuit:
#### not(bit0 bit1 + not (bit0 + bit1))
