Q- Write a python program which creates a tuple storing the first 15 digits of the Fibonacci series.
```python
n = int(input("Enter the number of terms:")) #here 15
fib = []
a,b = 0,1
for i in range(n):
    fib.append(a)
    a,b = b,a+b
t = tuple(fib)
print("Fibonacci Series",t)
```
OUTPUT-
```text
Fibonacci Series (0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377)
```
Q- Write a code snippet in python to display the element of list thrice if it is a number and display the element terminated with '$' if it is not a number.
```python
list1 = [56,'Geet','Anoop',100,'Rinku']
for word in list1:
    if type(word) == int:
        print(str(word) * 3)
    else:
        print(word+'$')
```
OUTPUT-
```text
565656
Geet$
Anoop$
100100100
Rinku$
```
Q- Find and write the output of the following code.
```python
Lst1 = ["20","50","30","40"]
CNT = 3
Sum = 0
for I in [7,5,4,6]:
    T = Lst1[CNT]
    Sum = float(T) + I
    print(Sum)
    CNT-=1
```
OUTPUT-
```text
47.0
35.0
54.0
26.0
```
Q- Write a python program to count the number of characters (character frequency) in a string.
   Sample string: 'google.com'
```python
str1 = 'google.com'
char_count = {}
for n in str1:
    if n in char_count:
        char_count[n] += 1
    else:
        char_count[n] = 1
print('Character Frequency:',char_count)
```
OUTPUT-
```text
Character Frequency: {'g': 2, 'o': 3, 'l': 1, 'e': 1, '.': 1, 'c': 1, 'm': 1}
```
Q- Write  python program to get a string from the given string where all occurences of its first char have been changed to '$', except the first char itself.
```python
str1 = 'restart'
char = str1[0]
str1 = str1.replace(char,'$')
result = char + str1
print('Modified String:',result)
```
OUTPUT-
```text
Modified String: r$esta$t
```
Q- Write a python progra to remove the nth index character from a non-empty string.
```python
str = 'python'
indexes_to_remove = [0,3,5]
for n in indexes_to_remove:
    firt_part = str[:n]
    last_part = str[n+1:]
    modified_str = firt_part + last_part
    print('Modified Index',n,":",modified_str)
```
OUTPUT-
```text
Modified Index 0 : ython
Modified Index 3 : pyton
Modified Index 5 : pytho
```
Q- W Rewrite the following code in python after removing all syntax error(s). underline each correction done in the code.
```python
p = 30
for c in rnage(0,p):
    If c%4==0:
        print (c*4)
Elseif c%5==0:
        print (c*3)
else
        print(c+10)
```
OUTPUT-
```python
p = 30
for c in range(0,p):
    if c%4==0:        
        print(c*4)
    elif c%5==0:      
        print(c*3)
    else:             
        print(c+10)
```
Q- Write A Python program to count the number of elements in a list within a specified range.
```python
list1 = [10, 20, 30, 40, 40, 40, 70, 80, 99]
min_val = 40
max_val = 100
ctr = 0
for x in list1:
    if min_val <= x <= max_val:
        ctr += 1
print("Number of elements in list1 within range(",min_val,"to",max_val,"):",ctr)
list2 = ['a','b','c','d','e','f']
min_char = 'a'
max_char = 'e'
ctr = 0
for x in list2:
    if min_char <= x <= max_char:
        ctr += 1
print("Number of elements in list2 within range(",min_char,"to",max_char,"):",ctr)
```
OUTPUT-
```
Number of elements in list1 within range( 40 to 100 ): 6
Number of elements in list2 within range( a to e ): 5
```
Q- Write the output displayed on execution of the following Python code.
```python
LS = ["HIMALAYA","NILGIRI","ALASKA","ALPS"]
D = {}
for S in LS:
    if len(S)%4 == 0:
        D[S] = len(S)
for K in D:
    print(K,D[K], sep = "#")
```
```
HIMALAYA#8
ALPS#4
```
Q- Write a program that fills a list with numbers. (Using randint())
```python
# A function that fills a list with numbers

from random import randint

def fill_list(lst,limit_num, low, high):
    for i in range(limit_num):
        lst.append(randint(low,high))

minimum = int(input("Min: "))
maximum = int(input("Max: "))
n = int(input("Numbers limit: "))
a = [] #an empty list
fill_list(a,n,minimum,maximum)
print(a) # Prints the newly created List
```
OUTPUT-
```
Min: 10
Max: 50
Numbers limit: 5
[36, 37, 48, 11, 221]
```
Q- Write a program to perform binary search using randint()
```python
from random import randint

def bin_search(lst, item):
    mid= len(lst)//2 #integer division
    low = 0
    high = len(lst) - 1
    while lst[mid] != item and low <= high:
        if item > lst[mid]:
            low = mid + 1
        else:
            high = mid - 1
        mid = (low + high) // 2
    if low > high:
        return None
    else:
        return mid
a = []
for i in range(10):
    a.append(randint(1,120)) #list elements within range get automatically generated
a.sort() #sort() used to arrange the list elements in  ascending order
value = int(input("Enter the number to be searched: "))
#index = bin_search(a,value)
print("Element found at the index: ", bin_search(a,value))
```
OUTPUT-
```text
Enter the number to be searched: 110
Element found at the index:  7
```
Q- To write a user-defined function to print a right-angled triangle.
```python
def triangle():
    '''
    Objective: To print a right-angled triangle
    Input Parameter: None
    Return value: None
    '''
    '''
    Approach: To use a print statement for each line of output
    '''
    print('*')
    print('* *')
    print('* * *')
    print('* * * *')
```
OUTPUT-
```
>>> triangle()
*
* *
* * *
* * * *
```
Q- Write a program to add and subtract two values and return the calculated result.
```python
#program to illustrate return statement returning multiple values
def add_diff(x, y):
    add = x + y
    diff = x - y
    return add, diff
a, b = add_diff(200,180)
print("The sum of two numbers is:", a)
print("The difference of two numbers is ", b)
```
OUTPUT-
```text
The sum of two numbers is: 380
The difference of two numbers is 20
```
Q- Modification of the above program to compute basic calculations performed in a calculator.
```python
def calc(a,b):
    add = a + b
    sub = a - b
    mul = a * b
    div = a / b
    return add, sub, mul, div
result = calc(500,40)
print("The result can be displayed as: ")
for i in result:    #displaying multiple values returned as the output
    print(i)
```
OUTPUT-
```
(540, 460, 20000, 12.5)
The result can be displayed as:
540
460
20000
12.5
```
Q- Write a python program to compute area of a rectangle by taking length and breadth as input.
```python
def areaRectangle(length, breadth = 1):
    area = length * breadth
    return area
def main():
    print('Enter the following values for rectangle:')
    lengthrect = int(input('Length: Integer Value: '))
    breadthrect = int(input('Breadth: Integer Value: '))
    arearect = areaRectangle(lengthrect, breadthrect)
    print('Area of the rectangle is: ', arearect)
if __name__ == '__main__':
    main()
```
OUTPUT-
```
Enter the following values for rectangle:
Length: Integer Value: 50
Breadth: Integer Value: 30
Area of the rectangle is: 1500
```
Q- What possible output(s) will be displayed on screen on the time of executionof the following code?
```python
import random
DATA = [120,130,240,350,460,570]
X=random.randint(1,3)
Y=random.randint(2,4)
for I in range(X):
    print(DATA[I],end=" #")
```
OUTPUT- 
```text
120 #130 #
```