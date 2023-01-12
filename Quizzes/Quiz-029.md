# Tasks
A. Create a function that receives a dictionary with letters in the alphabet as keys and a string. The functions returns the dictionary with a count as value for the occurrence of each letter:

|                 Input lexicon:dict, msg:str                 |            Output :str           |
|:-----------------------------------------------------------:|:--------------------------------:|
|              {‘w’:0,‘l’:0,‘c’:0}, “hello world”             |       {‘w’:1, ‘l’:3, ‘c’:0}      |
| {‘a’:0,‘e’:0,‘i’:0,‘o’:0,‘u’:0}, <br>“Why did I choose CS?” | {‘a’:0,‘e’:1,‘i’:1,‘o’:2,‘u’:0}, |

case1 = count_letters(my_dict, msg)
print(case1)

B. How many different colors could you represent in a 6 bit computer?

## Part A

### Code:

```.py
def count_letters(lexicon:dict,msg:str):
    for letter in msg:
        if letter in lexicon.keys():
            lexicon[letter] += 1
    return lexicon

print(count_letters({'w':0,'l':0,'c':0},"hello world"))
print(count_letters({'a':0,'e':0,'i':0,'o':0,'u':0},"Why did I choose CS?"))
```
