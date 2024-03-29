# HCF-of-a-Number-Using-Recursion-in-Python

HCF of a Number using Recursion
on this page we will learn to create a python program to find HCF of a Number using Recursion.

HCF – Highest common factor of two or more number such that it can completely divide all the numbers.

Example :

Input : first = 23, second = 69
Output : HCF of 23 and 69 is 23
Explanation : No other number in greater then 23 can divide both 23 and 69 completely. That’s why 23 is HCF of 23 & 69
LCM of a number in Python

Method 1 : Using Recursion
Algorithm
Start by making a function and passing both number to it as a and b
If b is equals to zero return a
Else return recursive call for the function with values b and remainder when a is divided by b respectively
Python Program to find HCF of a Number
To Learn more about Recursion   click here
Python Code
Run
def hcf(a, b):
    if b == 0:
        return a
    else:
        return hcf(b, a % b)


first = 23
second = 69

print('HCF of', first, 'and', second, 'is', hcf(first, second))
Output :

HCF of 23 and 69 is 23
Method 2 : Using Loop
Algorithm
Start by making a function and passing both number to it as a and b
If maximum between a & b is divided by minimum between a & b gives remainder zero return minimum between a & b
Iterate using for loop between range one more then half of minimum between a & b to 0 in reverse order using variable i
For each iteration check if  a divided by i and b divided by i both are equals to 0 then return i
Python Code
Run
def hcf(a, b):
    if max(a, b) % min(a, b) == 0:
        return min(a, b)
    for i in range(1 + min(a, b) // 2, 0, -1):
        if a % i == b % i == 0:
            return i


first = 23
second = 69

print('HCF of', first, 'and', second, 'is', hcf(first, second))
Output :

HCF of 23 and 69 is 23
