# Learning-Python

Here are some problems and you have to write a function for each problem. As you progress the problem gets more difficult (answers included).

**Problem 1** - printHello()

>Define a function that prints "Hello"


```python
def printHello():
    print("Hello")
```


**Problem 2** - checkDog(string)

>Define a function that returns True if the string contrains the word "dog", else False.


```python
def checkDog(string)
    #This will only check for "dog" with lower case "d"
    return 'dog' in string
    
    #This will check check both lowercase and uppercase
    return 'dog' in string.lower()
```

**Probelm 3** - pigLatin(string)

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

**Problem 4** - alternatingCapital(string)

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

**Problem 5** - lesserOfTwoEven(a,b)

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

**Problem 6** - animalCracker(string)

>Define a function, that takes two strings and return true if both string starts with the same letter

>* EX: animalCracker("Wild Wolf"), return True

>* EX: animalCracker("Cracky Kangaroo"), return False

>* HINT: use .split()

```python
def animalCracker(text):

    ans = text.lower().split()
    return ans[0][0]==ans[1][0]
```

**Problem 7** - makesTwenty(a,b)

>Define a function, that takes in two number and return true if either number is "20" or the sum of two number is "20"

```python
def makesTwenty(a,b):

    return a == 20 or b ==20 or (a+b) ==20

```

**Problem 8** - oldMacDonald(name)
> Define a fuction that takes in a name and capitalize the first and the fourth letter of the name

>* EX: oldMacDonald("macdonald"), Return "MacDonald"

>* EX: oldMacDonald("james"), Return "JamEs"

>* EX: oldMacDonald("tom"), Returns "Tom"

```python
def oldMacdonald(name = "Name"):

    ans = ""
    for i in range(len(name)):
        if i == 0 or i == 3:
            ans+=name[i].upper()
        else:
            ans+=name[i].lower()
    
    return ans
```
