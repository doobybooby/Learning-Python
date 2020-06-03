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

>Pig Latin: 
> If the string DOESN'T start with a VOWEL, return the string + "ay". If the string START with a VOWEL, return the string without the first letter + "first letter" + "ay"

> Example, pigLatin("banana"). Return "banana ay"
> Example, pigLatin("elevator"). Returns "levator eay" 

```python
#grab the first letter
    firstLet = mystr[0]
    
    #check if first letter is a vowel 
    if firstLet in 'aeiou':
        print("Starts with a vowel")
        return mystr[1:]+firstLet+"ay"
    else:
        print("doesn't tarts with a vowel")
        return mystr+"ay"
```
