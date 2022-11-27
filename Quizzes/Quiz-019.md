## 10.28.2022 Quiz #019

19. Create a function that changes the vowels in a string to numbers such as a=4,e=3,i=1,o=0 and space by _.

------------------------------------------------------------------------

Program:
```.py
def get_l3tt3r(msg:str):
    output = ''
    for letter in msg:
        if letter == 'i':
            output += '1'
        elif letter == 'a':
            output += '4'
        elif letter == 'e':
            output += '3'
        elif letter == 'o':
            output += '0'
        elif letter == ' ':
            output += '_'
        else:
            output += letter
    return output

print(get_l3tt3r("Hello World"))
print(get_l3tt3r("Why did I choose CS?"))
print(get_l3tt3r("Remember the Figure Caption"))
```

------------------------------------------------------------------------

Proof:
### Fig.1
Input: "Hello World", "Why did I choose CS?", "Remember the Figure Caption" | Output: H3ll0_W0rld, Why_d1d_I_ch00s3_CS?, R3m3mb3r_th3_F1gur3_C4pt10n
<img width="1047" alt="Screen Shot 2022-11-28 at 1 00 03" src="https://user-images.githubusercontent.com/112055140/204144785-4c60568c-6f82-4314-89b2-f55936b35a49.png">


------------------------------------------------------------------------

### Boolean Circut:
#### AB + not(B+C) + B(notC notA)
