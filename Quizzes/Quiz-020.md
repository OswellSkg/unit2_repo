## 01.11.2022 Quiz #20

Create a function that produces the table of Truth for 3 inputs:

------------------------------------------------------------------------

Program:
```.py
def get_truth():
    print("| A | B | C |")
    for i in range(8):
        print("|",i//4,"|",i//2%2,"|",i%2,"|")

table = get_truth()
```

------------------------------------------------------------------------

Proof:
### Fig.1
Input: get_truth() | Output: Table of Truth for ABC inputs
<img width="1046" alt="Screen Shot 2022-11-28 at 1 04 23" src="https://user-images.githubusercontent.com/112055140/204144982-39923fdd-4967-4f27-87c2-67f7b1d0372f.png">

------------------------------------------------------------------------

### Truth Table and Circut:
####Light = S1S2+(S2+S3(notS1))S1
