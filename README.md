# Learning-Python

Here are some problems and you have to write a function for each problem. As you progress the problem gets more difficult (answers included).

**Problem 1**

>Define a function that prints "Hello"

>* _HINT: Input nothing, return "Hello"_

```python
def printHello():
    print("Hello")
```


**Problem 2**

>Define a function that returns True if the string contrains the word "dog"

>* _HINT: Input a string, returns T/F

```python
def checkDog(string)
    #This will only check for "dog" with lower case "d"
    return 'dog' in string
    
    #This will check check both lowercase and uppercase
    return 'dog' in string.lower()
```

**Probelm 3**

>Define a fuction that returns the Pig Latin of the string

> Pig Latin: 
> If the string DOESN'T start with a VOWEL, return the string + "ay". If the string START with a VOWEL, return the string without the first letter + "first letter" + "ay"

> * Example, pigLatin("banana"). Return "banana ay"

> * Example, pigLatin("elevator"). Returns "levator eay" 

> * HINT: slice and index 

```python
#grab the first letter
def pigLatin(mystr)
    firstLet = mystr[0]
    
    #check if first letter is a vowel 
    if firstLet in 'aeiou':
        return mystr[1:]+firstLet+"ay"
    else:
        return mystr+"ay"
```

**Problem 4**

>Define a function that capitalizes every other letter

>* EX: "aBcDeF"

>* HINT: convert everything to lower case first and concatinate  

```python
def alternatingCapital(string):
   
    ans = ""
    
    for i in range(len(string)):
        if i%2==1:
            ans += string[i].lower()
        else:
            ans += string[i].upper()
    return ans


```

**Problem 5**

>Define a function, that takes in two numbers, and if both numbers are even return the lower number, else return the lower number

>* EX: lesserOfTwoEven(4,10), Returns 4

>* EX: lesserOfTwoEven(5,11), Return 11

>* EX: lesserOfTwoEven(8,13), Return 13

```python
def lesserOfTwoEven(a,b):
 
    if a%2==0 and b%2 ==0:
        return min(a,b)
    else:
        return max(a,b)
```
