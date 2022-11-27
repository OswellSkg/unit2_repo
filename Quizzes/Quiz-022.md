## 08.11.22 Quiz #022

Create a program that produces n random values from the equation below, <br>
where m and s are the other inputs of the function.

<img width="329" alt="Screen Shot 2022-11-28 at 1 40 35" src="https://user-images.githubusercontent.com/112055140/204148464-305047d6-63d7-4ef6-aeb8-dedc3f0e13ca.png">


------------------------------------------------------------------------

Program:
```.py
import random
random.seed(1234)

def equation(n=int,m=int,s=int):
    print("|  x  |  y(x)  |")
    for i in range(n):
        x = random.randint(0,100)
        y = x ** (1 / 2 * ((m / s) ** 2))
        y_str = f"{y:.2f}"
        print("|" + str(x).center(5) + "|" + y_str.center(8) + "|")

sample = equation(5,3,2)
```

------------------------------------------------------------------------

Proof:
### Fig.1
Input: 99, 56, 14, 0, 11 | Output: 175.83, 92.62, 19.47, 0.00, 14.84
<img width="1046" alt="Screen Shot 2022-11-28 at 1 41 13" src="https://user-images.githubusercontent.com/112055140/204148504-2bc57026-c535-4200-9c9e-705be9a775a2.png">

------------------------------------------------------------------------

### Prove:
#### A (A + B) = A
