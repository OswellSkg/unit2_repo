## 10.27.2022 Quiz#18

A match stick takes 5 seconds to burn completely. <br>
The length of the forest that Lily needs to cross is 1 meters. <br>
Lily's speed is s cm/s. <br>
What is the minimum number of match stcicks Lily needs to burn to cross the forest safely?

------------------------------------------------------------------------

Program:
```.py
import math

def numberMatches(l,s):
    matches = (l*20/s)
    return f"{math.ceil(matches)} matches"


print(numberMatches(100,100))
print(numberMatches(250, 110))
print(numberMatches(500, 150))
print(numberMatches(12345, 123))
```

------------------------------------------------------------------------

Proof:
### Fig.1
Input: (100,100),(250, 110),(500, 150),(12345, 123) | Output: 20 matches,46 matches,67 matches,2008 matches
<img width="1046" alt="Screen Shot 2022-11-27 at 23 26 53" src="https://user-images.githubusercontent.com/112055140/204140456-107a1483-a676-48af-88b6-8092a4ac0b96.png">

------------------------------------------------------------------------
