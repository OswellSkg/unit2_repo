## 04.11.2022 Quiz #021

Using the function that produces the table of Truth for 3 inputs, add a column for the boolean equation
AB+(not B)+(notB C)

------------------------------------------------------------------------

Program:
```.py
def get_truth():
    print("| A | B | C | AB + not B + not CB |")
    for i in range(8):
        a = i//4
        b = i//2%2
        c = i%2
        d = int(a and b) or int(not b) or int(not b and c)
        print(f"|{str(a).center(3)}|{str(b).center(3)}|{str(c).center(3)}|{str(d).center(21)}|")

table = get_truth()
```

------------------------------------------------------------------------

Proof:
### Fig.1
Input: A, B, C, AB+(not B)+(notB C) | Output: Truth Table
<img width="1047" alt="Screen Shot 2022-11-28 at 1 28 17" src="https://user-images.githubusercontent.com/112055140/204146527-388b2de9-a5d7-41dc-9cd6-762409896537.png">

------------------------------------------------------------------------

### Truth table and Circuit:
#### X = ZW ⨁ (Z ⨁ Y(not W)) 
