# Python programming exercises for Python 3

### Question 1
Solution:
```python
l=[]
for i in range(2000, 3201):
    if (i%7==0) and (i%5!=0):
        l.append(str(i))

print(','.join(l))
```

### Question 2
Solution:
```python
def fact(x):
    if x == 0:
        return 1
    return x * fact(x - 1)

x=int(input())
print(fact(x))
```

### Question 3
Solution:
```python
n=int(input())
d=dict()
for i in range(1,n+1):
    d[i]=i*i

print(d)
```

### Question 4
Solution:
```python
values=input()
l=values.split(",")
t=tuple(l)
print(l)
print(t)
```
### Question 5
Solution:
```python
class InputOutString(object):
    def __init__(self):
        self.s = ""

    def getString(self):
        self.s = input()
    
    def printString(self):
        print(self.s.upper())

strObj = InputOutString()
strObj.getString()
strObj.printString()
```

### Question 6
Solution:
```python
import math
c=50
h=30
value = []
items=[x for x in input().split(',')]
for d in items:
    value.append(str(int(round(math.sqrt(2*c*float(d)/h)))))

print(','.join(value))
```
### Question 7
Solution:
```python
input_str = input()
dimensions=[int(x) for x in input_str.split(',')]
rowNum=dimensions[0]
colNum=dimensions[1]
multilist = [[0 for col in range(colNum)] for row in range(rowNum)]

for row in range(rowNum):
    for col in range(colNum):
        multilist[row][col]= row*col

print(multilist)
```
### Question 8
Solution:
```python
items=[x for x in input().split(',')]
items.sort()
print(','.join(items))
```

### Question 9
Solution:
```python
lines = []
while True:
    s = input()
    if s:
        lines.append(s.upper())
    else:
        break;

for sentence in lines:
    print(sentence)
```

### Question 10
Solution:
```python
s = input()
words = [word for word in s.split(" ")]
print(" ".join(sorted(list(set(words)))))
```
### Question 11
Solution:
```python
value = []
items=[x for x in input().split(',')]
for p in items:
    intp = int(p, 2)
    if not intp%5:
        value.append(p)

print(','.join(value))
```
### Question 12
Solution:
```python
values = []
for i in range(1000, 3001):
    s = str(i)
    if (int(s[0])%2==0) and (int(s[1])%2==0) and (int(s[2])%2==0) and (int(s[3])%2==0):
        values.append(s)
print(",".join(values))
```

### Question 13
Solution:
```python
s = input()
d={"DIGITS":0, "LETTERS":0}
for c in s:
    if c.isdigit():
        d["DIGITS"]+=1
    elif c.isalpha():
        d["LETTERS"]+=1
    else:
        pass
print("LETTERS", d["LETTERS"])
print("DIGITS", d["DIGITS"])
```
### Question 14
Solution:
```python
s = input()
d={"UPPER CASE":0, "LOWER CASE":0}
for c in s:
    if c.isupper():
        d["UPPER CASE"]+=1
    elif c.islower():
        d["LOWER CASE"]+=1
    else:
        pass
print("UPPER CASE", d["UPPER CASE"])
print("LOWER CASE", d["LOWER CASE"])
```

### Question 15
Solution:

```python
a = input()
n1 = int( "%s" % a )
n2 = int( "%s%s" % (a,a) )
n3 = int( "%s%s%s" % (a,a,a) )
n4 = int( "%s%s%s%s" % (a,a,a,a) )
print(n1+n2+n3+n4)
```
### Question 16
Solution:

```python
values = input()
numbers = [x for x in values.split(",") if int(x)%2!=0]
print(",".join(numbers))
```
### Question 17
Solution:

```python
netAmount = 0
while True:
    s = input()
    if not s:
        break
    values = s.split(" ")
    operation = values[0]
    amount = int(values[1])
    if operation=="D":
        netAmount+=amount
    elif operation=="W":
        netAmount-=amount
    else:
        pass
print(netAmount)
```
### Question 18
Solutions:

```python
import re
value = []
items=[x for x in input().split(',')]
for p in items:
    if len(p)<6 or len(p)>12:
        continue
    else:
        pass
    if not re.search("[a-z]",p):
        continue
    elif not re.search("[0-9]",p):
        continue
    elif not re.search("[A-Z]",p):
        continue
    elif not re.search("[$#@]",p):
        continue
    elif re.search("\s",p):
        continue
    else:
        pass
    value.append(p)
print(",".join(value))
```
### Question 19
Solutions:
from operator import itemgetter, attrgetter

```python
l = []
while True:
    s = input()
    if not s:
        break
    l.append(tuple(s.split(",")))

print(sorted(l, key=itemgetter(0,1,2)))
```

### Question 20
Solution:

```python
def putNumbers(n):
    i = 0
    while i<n:
        j=i
        i=i+1
        if j%7==0:
            yield j

for i in reverse(100):
    print(i)
```
### Question 21
Solution:

```python
import math
pos = [0,0]
while True:
    s = input()
    if not s:
        break
    movement = s.split(" ")
    direction = movement[0]
    steps = int(movement[1])
    if direction=="UP":
        pos[0]+=steps
    elif direction=="DOWN":
        pos[0]-=steps
    elif direction=="LEFT":
        pos[1]-=steps
    elif direction=="RIGHT":
        pos[1]+=steps
    else:
        pass

print(int(round(math.sqrt(pos[1]**2+pos[0]**2))))
```
### Question 22
Solution:

```python
freq = {}   # frequency of words in text
line = input()
for word in line.split():
    freq[word] = freq.get(word,0)+1

words = freq.keys()
words.sort()

for w in words:
    print("%s:%d" % (w,freq[w]))
```
### Question 23
Solution:

```python
def square(num):
    return num ** 2

print(square(2))
print(square(3))
```
### Question 24
Solution:
```python
print(abs.__doc__)
print(int.__doc__)
print(input.__doc__)

def square(num):
    '''Return the square value of the input number.
    
    The input number must be integer.
    '''
    return num ** 2

print(square(2))
print(square.__doc__)
```
### Question 25
Solution:
```python
class Person:
    # Define the class parameter "name"
    name = "Person"
    
    def __init__(self, name = None):
        # self.name is the instance parameter
        self.name = name

jeffrey = Person("Jeffrey")
print("%s name is %s" % (Person.name, jeffrey.name))

nico = Person()
nico.name = "Nico"
print("%s name is %s" % (Person.name, nico.name))
```

### Question 26
Solution

```python
def SumFunction(number1, number2):
	return number1+number2

print(SumFunction(1,2))
```
### Question 27
Solution
```python
def printValue(n):
    print(str(n))

printValue(3)
```

### Question 28
Solution
```python
def printValue(n):
    print(str(n))

printValue(3)
```
### Question 29
Solution
```python
def printValue(s1,s2):
    print(int(s1)+int(s2))

printValue("3","4")
```

### Question 30
Solution
```python
def printValue(s1,s2):
    print(s1+s2)

printValue("3","4") #34
```

### Question 31
Solution
```python
def printValue(s1,s2):
    len1 = len(s1)
    len2 = len(s2)
    if len1>len2:
        print(s1)
    elif len2>len1:
        print(s2)
    else:
        print(s1)
        print(s2)
        
printValue("one","three")

```
### Question 32
Solution
```python
def checkValue(n):
    if n%2 == 0:
        print("It is an even number")
    else:
        print("It is an odd number")
        
checkValue(7)
```
### Question 33
Solution
```python
def printDict():
    d=dict()
    d[1]=1
    d[2]=2**2
    d[3]=3**2
    print(d)
        
printDict()
```
### Question 34
Solution
```python
def printDict():
	d=dict()
	for i in range(1,21):
		d[i]=i**2
	print(d)

printDict()
```
### Question 35
Solution
```python
def printDict():
	d=dict()
	for i in range(1,21):
		d[i]=i**2
	for (k,v) in d.items():	
		print(v)

printDict()
```
### Question 36
Solution
```python
def printDict():
	d=dict()
	for i in range(1,21):
		d[i]=i**2
	for k in d.keys():	
		print(k)

printDict()
```

### Question 37
Solution
```python
def printList():
	li=list()
	for i in range(1,21):
		li.append(i**2)
	print(li)

printList()
```
### Question 38
Solution
```python
def printList():
	li=list()
	for i in range(1,21):
		li.append(i**2)
	print(li[:5])

printList()
```
### Question 39
Solution
```python
def printList():
	li=list()
	for i in range(1,21):
		li.append(i**2)
	print(li[-5:])

printList()
```
### Question 40
Solution
```python
def printList():
	li=list()
	for i in range(1,21):
		li.append(i**2)
	print li[5:]

printList()
```
### Question 41
Solution
```python
def printTuple():
	li=list()
	for i in range(1,21):
		li.append(i**2)
	print(tuple(li))
		
printTuple()
```
### Question 42
Solution
```python
tp=(1,2,3,4,5,6,7,8,9,10)
tp1=tp[:5]
tp2=tp[5:]
print(tp1)
print(tp2)
```

### Question 43
Solution
```python
tp=(1,2,3,4,5,6,7,8,9,10)
li=list()
for i in tp:
	if tp[i]%2==0:
		li.append(tp[i])

tp2=tuple(li)
print(tp2)
```
### Question 44
Solution
```python
s= raw_input()
if s=="yes" or s=="YES" or s=="Yes":
    print "Yes"
else:
    print "No"
```
### Question 45
Solution
```python
li = [1,2,3,4,5,6,7,8,9,10]
evenNumbers = filter(lambda x: x%2==0, li)
print(evenNumbers)
```

### Question 46
Solution
```python
li = [1,2,3,4,5,6,7,8,9,10]
squaredNumbers = map(lambda x: x**2, li)
print(squaredNumbers)
```
### Question 47
Solution
```python
li = [1,2,3,4,5,6,7,8,9,10]
evenNumbers = map(lambda x: x**2, filter(lambda x: x%2==0, li))
print(evenNumbers)
```
### Question 48
Solution
```python
evenNumbers = filter(lambda x: x%2==0, range(1,21))
print(evenNumbers)
```
### Question 49
Solution
```python
squaredNumbers = map(lambda x: x**2, range(1,21))
print(squaredNumbers)
```
### Question 50
Solution
```python
class American(object):
    @staticmethod
    def printNationality():
        print("America")

anAmerican = American()
anAmerican.printNationality()
American.printNationality()
```
### Question 51
Solution:
```python
class American(object):
    pass

class NewYorker(American):
    pass

anAmerican = American()
aNewYorker = NewYorker()
print(anAmerican)
print(aNewYorker)
```
### Question 52
Solution:
```python
class Circle(object):
    def __init__(self, r):
        self.radius = r

    def area(self):
        return self.radius**2*3.14

aCircle = Circle(2)
print aCircle.area()
```

### Question 53
Solution:
```python
class Rectangle(object):
    def __init__(self, l, w):
        self.length = l
        self.width  = w

    def area(self):
        return self.length*self.width

aRectangle = Rectangle(2,10)
print(aRectangle.area())
```
### Question 54
Solution:
```python
class Shape(object):
    def __init__(self):
        pass

    def area(self):
        return 0

class Square(Shape):
    def __init__(self, l):
        Shape.__init__(self)
        self.length = l

    def area(self):
        return self.length*self.length

aSquare= Square(3)
print(aSquare.area())
```

### Question 55
Solution:

```python
raise RuntimeError('something wrong')
```
### Question 56
Solution:
```python
def throws():
    return 5/0

try:
    throws()
except ZeroDivisionError:
    print("division by zero!")
except Exception, err:
    print('Caught an exception')
finally:
    print('In finally block for cleanup')
```
### Question 57
Solution:
```python
class MyError(Exception):
    """My own exception class

    Attributes:
        msg  -- explanation of the error
    """
    
    def __init__(self, msg):
        self.msg = msg

error = MyError("something wrong")
```

### Question 58
Solution:
```python
import re
emailAddress = raw_input()
pat2 = "(\w+)@((\w+\.)+(com))"
r2 = re.match(pat2,emailAddress)
print(r2.group(1))
```
### Question 59
Solution:
```python
import re
emailAddress = raw_input()
pat2 = "(\w+)@(\w+)\.(com)"
r2 = re.match(pat2,emailAddress)
print(r2.group(2))
```

### Question 60
Solution:
```python
import re
s = raw_input()
print(re.findall("\d+",s))
```

### Question 61
Solution:
```python
unicodeString = u"hello world!"
print(unicodeString)
```
### Question 62
Solution:
```python
s = input()
u = unicode( s ,"utf-8")
print(u)
```
### Question 63
Solution:
```python

# -*- coding: utf-8 -*-

#----------------------------------------#
```
### Question 64
Solution:
```python
n=int(input())
sum=0.0
for i in range(1,n+1):
    sum += float(float(i)/(i+1))
print(sum)
```
### Question 65
Solution:
```python
def f(n):
    if n==0:
        return 0
    else:
        return f(n-1)+100

n=int(input())
print(f(n))
```
### Question 66
Solution:
```python
def f(n):
    if n == 0: return 0
    elif n == 1: return 1
    else: return f(n-1)+f(n-2)

n=int(input())
print(f(n))
```
### Question 67
Solution:
```python
def f(n):
    if n == 0: return 0
    elif n == 1: return 1
    else: return f(n-1)+f(n-2)

n=int(input())
values = [str(f(x)) for x in range(0, n+1)]
print(",".join(values))
```
### Question 68
Solution:
```python
def EvenGenerator(n):
    i=0
    while i<=n:
        if i%2==0:
            yield i
        i+=1


n=int(input())
values = []
for i in EvenGenerator(n):
    values.append(str(i))

print(",".join(values))
```
### Question 69
Solution:
```python
def NumGenerator(n):
    for i in range(n+1):
        if i%5==0 and i%7==0:
            yield i

n=int(input())
values = []
for i in NumGenerator(n):
    values.append(str(i))

print(",".join(values))
```
### Question 70
Solution:
```python
li = [2,4,6,8]
for i in li:
    assert i%2==0
```
### Question 71
Solution:
```python
expression = raw_input()
print(eval(expression))
```
### Question 72
Solution:
```python
import math
def bin_search(li, element):
    bottom = 0
    top = len(li)-1
    index = -1
    while top>=bottom and index==-1:
        mid = int(math.floor((top+bottom)/2.0))
        if li[mid]==element:
            index = mid
        elif li[mid]>element:
            top = mid-1
        else:
            bottom = mid+1

    return index

li=[2,5,7,9,11,17,222]
print(bin_search(li,11))
print(bin_search(li,12))
```
### Question 73
Solution:
```python
import math
def bin_search(li, element):
    bottom = 0
    top = len(li)-1
    index = -1
    while top>=bottom and index==-1:
        mid = int(math.floor((top+bottom)/2.0))
        if li[mid]==element:
            index = mid
        elif li[mid]>element:
            top = mid-1
        else:
            bottom = mid+1

    return index

li=[2,5,7,9,11,17,222]
print(bin_search(li,11))
print(bin_search(li,12))
```

### Question 74
Solution:
```python
import random
print(random.random()*100)
```
### Question 75
Solution:
```python
import random
print(random.random()*100-5)
```
### Question 76
Solution:
```python
import random
print(random.choice([i for i in range(11) if i%2==0]))
```
### Question 77
Solution:
```python
import random
print(random.choice([i for i in range(201) if i%5==0 and i%7==0]))
```

### Question 78
Solution:
```python
import random
print(random.sample(range(100), 5))
```
### Question 79
Solution:
```python
import random
print(random.sample([i for i in range(100,201) if i%2==0], 5))
```
### Question 80
Solution:
```python
import random
print(random.sample([i for i in range(1,1001) if i%5==0 and i%7==0], 5))
```
### Question 81
Solution:
```python
import random
print(random.randrange(7,16))
```
### Question 82
Solution:
```python
import zlib
s = b'hello world!hello world!hello world!hello world!'
t = zlib.compress(s)
print(t)
print(zlib.decompress(t))
```
### Question 83
Solution:
```python
from timeit import Timer
t = Timer("for i in range(100):1+1")
print(t.timeit())
```

### Question 84
Solution:
```python
from random import shuffle
li = [3,6,7,8]
shuffle(li)
print(li)
```
### Question 85
Solution:
```python
from random import shuffle
li = [3,6,7,8]
shuffle(li)
print(li)
```
### Question 86
Solution:
```python
subjects=["I", "You"]
verbs=["Play", "Love"]
objects=["Hockey","Football"]
for i in range(len(subjects)):
    for j in range(len(verbs)):
        for k in range(len(objects)):
            sentence = "%s %s %s." % (subjects[i], verbs[j], objects[k])
            print(sentence)
```
### Question 87
Solution:
```
li = [5,6,77,45,22,12,24]
li = [x for x in li if x%2!=0]
print(li)
```
### Question 88
Solution:
```
li = [12,24,35,70,88,120,155]
li = [x for x in li if x%5!=0 and x%7!=0]
print(li)
```
### Question 89
Solution:
```python
li = [12,24,35,70,88,120,155]
li = [x for (i,x) in enumerate(li) if i%2!=0]
print(li)
```
### Question 90
Solution:
```
array = [[ [0 for col in range(8)] for col in range(5)] for row in range(3)]
print(array)
```
### Question 91
Solution:
```python
li = [12,24,35,70,88,120,155]
li = [x for (i,x) in enumerate(li) if i not in (0,4,5)]
print(li)
```
### Question 92
Solution:
```python
li = [12,24,35,24,88,120,155]
li = [x for x in li if x!=24]
print(li)
```
### Question 93
Solution:
```python
set1=set([1,3,6,78,35,55])
set2=set([12,24,35,24,88,120,155])
set1 &= set2
li=list(set1)
print(li)
```
### Question 94
Solution:
```python
def removeDuplicate( li ):
    newli=[]
    seen = set()
    for item in li:
        if item not in seen:
            seen.add( item )
            newli.append(item)

    return newli

li=[12,24,35,24,88,120,155,88,120,155]
print(removeDuplicate(li))
```
### Question 95
Solution:
```python
class Person(object):
    def getGender( self ):
        return "Unknown"

class Male( Person ):
    def getGender( self ):
        return "Male"

class Female( Person ):
    def getGender( self ):
        return "Female"

aMale = Male()
aFemale= Female()
print(aMale.getGender())
print(aFemale.getGender())
```

### Question 96
Solution:
```python
dic = {}
s=raw_input()
for s in s:
    dic[s] = dic.get(s,0)+1
print('\n'.join(['%s,%s' % (k, v) for k, v in dic.items()]))
```
### Question 97
Solution:
```python
s=raw_input()
s = s[::-1]
print(s)
```
### Question 98
Solution:
```python
s=raw_input()
s = s[::2]
print(s)
```
### Question 99
Solution:
```python
import itertools
print(list(itertools.permutations([1,2,3])))
```
### Question 100
Solution:
```python
def solve(numheads,numlegs):
    ns='No solutions!'
    for i in range(numheads+1):
        j=numheads-i
        if 2*i+4*j==numlegs:
            return i,j
    return ns,ns

numheads=35
numlegs=94
solutions=solve(numheads,numlegs)
print(solutions)
```

Adapted from [Python programming exercises](https://github.com/zhiwehu/Python-programming-exercises)
