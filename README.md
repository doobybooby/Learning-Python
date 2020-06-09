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

> * Key Concept: slice and index 

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

>* Key Concept: convert everything to lower case first and concatinate  

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

>* Key Concept: use .split()

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

**Problem 9** - masterYoda(text)
> Define a function that reverse the order of the text

>* EX: "How are you", Returns "you are How"

>* EX: "May the force be with you", Returns "you with be force the May"

```python
def masterYoda(text):
    
    listword = text.split()
    reversedList = listword[::-1]
    print(reversedList)
    return " ".join(reversedList)
```

**Problem 10** - almostThere(n)
>Define a function that returns True if the number is between 90-110 or 190-210, inclusive

>* EX: almostThere(10), Returns False

>* EX: almostThere(90), Returns True

```python
def almostThere(n):
  
    return (abs(100-n)<=10) or (abs(200-n)<=10)

```

**Problem 11** - has33(intlist)
> Define a function that checks if the list contains two consecutive 3.

>* EX: has33([1,2,3,4,5,6]), Returns False

>* EX: has33([1,2,3,3,4,5]), Returns True

```python 
def has33(nums):
    
    if len(nums)==1:
        return False
    else:
        for i in range(1,len(nums)):
            if nums[i] == 3 and nums[i-1]==3:
                return True
    
    return False

```

**Problem 12** - paperDoll(text)

> Define a function that will repeat each character three times

>* EX: "Hey", Returns "HHHeeeyyy"

>* EX: "race car", Returns "rrraaaccceee   cccaaarrr"

```python
def paperDoll(text):
    '''
    input a text
    output copy each letter of text 3 times
    example "hey -> hhheeeyyy"
    '''
    ans = ""
    for i in text:
        ans+=i+i+i
    return ans

```

**Problem 13** - blackJack(a,b,c)
> Define a function that does blackJack. If the sum of int a+b+c less than 21. Return the number. If at least one of a/b/c is 11 reduce it to 1 then return the sum. If the sum is greater than 21, return "Bust!"

>* EX: blackJack(4,5,8), Returns 17

>* EX: blackJack(11,8,7), Returns 16

```python 
def blackJack(a,b,c):

    if sum([a,b,c])<= 21:
        return a+b+c
    else:
        if 11 in [a,b,c] and sum([a,b,c])<=31:
            return a+b+c -10
        else:
            return "Bust!"
```

**Problem 14** - summerOf69(arrlist)
> Define a function that returns the sum of a list UNLESS, there is 6 then you don't add until there is a 9, then continue adding

>* EX: summerOf69([1,2,3,4,5]), Returns 15

>* EX: summerOf69([1,2,3,4,5,6,7,8,9), Returns 15

>* EX: summerOf69([2,3,6,4,9,5]), Returns 10

```python
def summerOf69(arr):

    total = 0
    add = True
    for num in arr:
        while add:
            if num!=6:
                total+=num
                break
            else:
                add = False
        while not add:
            if num!=9:
                break
            else:
                add = True
                break
    return total
```

**Problem 15** - spyGame(arr)
> Define a function that checks if the list contains the sequence 007.

>* EX: spyGame([1,2,0,0,7,3,4]), Returns True

>* EX: spyGame([1,0,2,0,3,7,4]), Returns True

>* EX: spyGame([1,0,7,0,2]), Returns False

>* HINT: you can solve this like the summerOf69 or creating a list [0,0,7] then use pop

```python

def spyGame(arr):

code = [0,0,7]
    for num in arr:
        if num == code[0]:
            code.pop(0)
    return len(code) == 0
```

**Probelm 16** - palindrome(s):

> Define a palindrome function. 

>* Palindrome is when a string is the same as if you read it backwards.

>* EX: palindrome("wow"), Return True

>* EX: palindrome("race car"), Return True

>* EX: palindrome("abbcdba") returns false

```python

def palindrome(s):
    rs = s[::-1]
    if s == rs:
        return True
    else:
        return False
```

