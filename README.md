# python_practice

# Python codes list-2


## Q-3) Convert ip address from “a.b.c.d” format into integer and vice versa


##converting IPv4 address to int

import ipaddress



addr1 = ipaddress.ip_address('191.255.254.40')

addr2 = ipaddress.ip_address('0.0.0.123')

print(int(addr1))

print(int(addr2))

##converting IPv6 address to int

addr3 = ipaddress.ip_address('2001:db7:dc75:365:220a:7c84:d796:6401')

print(int(addr3))

print("******************************************************")
##importing the module

import ipaddress

##converting int to IPv4 address

print(ipaddress.ip_address(3221225000))

print(ipaddress.ip_address(123))

##converting int to IPv6 address

print(ipaddress.ip_address(42540766400282592856903984001653826561))

## Q-4) Check whether given string is isogram or not
def check_isogram(string):
    string = string.lower()
    a = [x for x in list(set(list(string))) if x != ' ']
    b = [x for x in list(string) if x != ' ']
    if len(a) == len(b):
        return string + " is an Isogram"
    else:
        return string + " is not an Isogram"
print(check_isogram("document"))




## Q-5) given a string , find the mexican wave 

s='hello'
new=[]
for i, val in enumerate(s[:]):
    up=s[i].upper()
    c=s[:i] + up + s[i+1:]
    new.append(c)
print(new)


## Qno 6


test_str = '8669733688942'
an_integer,x = 0 , 0

K = 1

res = []
for idx in range(0, len(test_str), K):
    # converting to int, after slicing
    res.append(int(test_str[idx: idx + K]))

for i in range(len(res)):
    y = res.copy()
    y.pop(i)

    strings = [str(integer) for integer in y]
    a_string = "".join(strings)
    an_integer = int(a_string)
    if an_integer>x:
        x = an_integer
print(x)




## 7. Largest number by shuffling

a = 23546354723

strng_list = str(a)

digit_map = map(int,strng_list)

digit_list = list(digit_map)

##print(digit_list)

digit_list.sort(reverse=True)

##print(digit_list)

for i in digit_list:
    print(i, end= "") 

## 8. Word frequency 
word = 'Ajay Ajay ajaya ajaya '
data = {}
for i in word:
    if i in data:
        data[i] = data[i] + 1
    else:
        data[i] = 1
print(data)

## 9. RGB to HEX and HEX to RGB


r = 128
g = 96
b = 194
hexColor = '#%02x%02x%02x' % (r, g, b)

print(hexColor)

hexColor = '#8060c2'
r = int(hexColor[1:3], 16)
g = int(hexColor[3:5], 16)
b = int(hexColor[5:7], 16)

print(str(r) + ',' + str(g) + ',' + str(b))

## 10. accumulated string 
mylist = ("accumalated string")
num = 0
for i in mylist:
    num = num+1
    str1 = num*i
    print(str1)



# python code list-1


## ques 1.


l = [5,5,5,5,5,5,5,6]
l.sort()
print(l[-1])

## Q.2)

l=[10,21,35,11,78,2,5,1,65,69,87]
s = 0
for i in l:
    s+=i
avg = s/len(l)
print(avg)
l.sort()
print(l)
if avg in l:
    i = l.index(avg)
    print(l[i-1],l[i+1])
else:
    for x in l:
        if avg<x:
            b=x
            break
    print(l[l.index(b)-1],l[l.index(b)])


## Q.6)

l=[10,21,35,11,78,2,5,1,65,69,87]
l.sort()
print(l[1]-l[0])

## Q.7 

l = [1,2,3,4,5,6,7,8,9];
len_list = len(l)
sum = 0;
for i in range(len_list):
    sum = l[i]+sum;
avrg = sum/len_list;
#print(avrg);
l_counter = 0;
for i in range(len_list):
    if(l[i]<avrg):
        l_counter = l_counter+1;
print(l_counter);


