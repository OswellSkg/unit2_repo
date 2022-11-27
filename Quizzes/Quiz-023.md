## 10.11.22  Quiz#023

Create a program that produces the graph for the function in Quiz #22.
<img width="316" alt="Screen Shot 2022-11-28 at 1 49 34" src="https://user-images.githubusercontent.com/112055140/204148843-a8872f5e-f101-45ac-bc6c-16e38b0a0554.png">



------------------------------------------------------------------------

Program:
```.py
import random
random.seed(1234)

def equation(n=int,m=int,s=int):
    print(f"|{'x'.center(20)}|{'y'.center(20)}|")
    x_out = []
    y_out = []
    for i in range(n):
        x = random.randint(0,100)
        x_out.append(x)
        y = x ** (1 / 2 * ((m / s) ** 2))
        y_out.append(y)
        y_str = f"{y:.1f}"
        print(f"|{str(x).center(20)}|{y_str.center(20)}|")
    return y_out, x_out

data_y, data_x = equation(10,3,2)

from matplotlib import pyplot as plt
plt.plot(data_x, data_y, color="r", marker="o")
plt.xlabel("x")
plt.ylabel("$y=x^(1/2((m/s)^2)$")
plt.show()
```

------------------------------------------------------------------------

Proof:
### Fig.1
Input: Function from Quiz022 | Output: Graph
<img width="1656" alt="Screen Shot 2022-11-28 at 1 47 49" src="https://user-images.githubusercontent.com/112055140/204148775-7b06e4ea-6e4b-4077-a4fd-6fbdc9c6a900.png">

------------------------------------------------------------------------

### Truth table:
#### A(A ⊕ B) 
