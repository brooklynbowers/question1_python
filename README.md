## question1_python

write a program which will find all such numbers which are divisible by 7 
but are not a multiple of 5, between 2000 and 3200 (both included).
the numbers obtained should be printed in a comma-separated sequence on a single line.

code:

'list = []
for num in range(2000, 3200):
    if num%5 == 0:
        continue
    elif num % 7 == 0:
        list.append(num)

    else:
        continue

print(list)'
    
## forgot the following

*to check division:*
check if a is divisible by b
use:      'a % b == 0'

*to put something into a list*
list is the name of the list you are putting something into
the_thing is what you are adding to the list (this puts the_thing at the end of the list)
'append.list(the_thing)'    

instead of looping through 'if num % 5 == 0:' and then continuing, 
could have instead used 'if num % 5 != 0 and num % 7 == 0'
**!= is "not equal"**

## answer from ztm (python 2)

'for i in range(2000,3201):
    if i%7 == 0 and i%5!=0:
        print(i,end=',')
print("\b")'

## another answer from ztm (python 3)
'l=[]
for i in range(2000, 3201):
    if (i%7==0) and (i%5!=0):
        l.append(str(i))

print (','.join(l))'

## using generators and list comprehension
'print(*(i for i in range(2000, 3201) if i%7 == 0 and i%5 != 0), sep=",")'
