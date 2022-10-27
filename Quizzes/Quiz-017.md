## 10.25.2022 Quiz #17

# Header Comment: Create a function that produces the average letter length of the input list.

------------------------------------------------------------------------

Program:
```.py
def averageLength(given:list)->float:
    total = 0
    for i in given:
        total += len(i)
    return total/len(given)

for i in [["Hello","main"],["Peru","France","Nepal"],["Computer Science","Art"],["one","two"]]:
    print(i)
    print(averageLength(i))
    print("\n")
```

------------------------------------------------------------------------

Proof:
### Fig.1
Input: (("Hello","main"),("Peru","France","Nepal"),("Computer Science","Art"),("one","two")) | Output: (4.5,5.0,9.5,3.0)
<img width="1047" alt="Input: (("Hello","main"),("Peru","France","Nepal"),("Computer Science","Art"),("one","two")) | Output: (4.5,5.0,9.5,3.0)" src="https://user-images.githubusercontent.com/112055140/198179901-e84ffe89-527b-4258-a27c-d47d468f373b.png">

------------------------------------------------------------------------

### Flowchart:
