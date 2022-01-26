
### ADD DIGIT OF NUMBER
```javascript
a=int(input("Enter a Number:"))
b=0;
while(a>0):
    temp=a%10;
    b=temp+b;
    a=a//10;
    
print(b)
```
### TAKE INPUT FROM USER IN NUMBER LIST
```javascript
l=[]
l=input("Enter a Number.").split(",")
for i in l:
    print(i);
```

### Program to print 1 to 100 ,skippng number which is divisible by 3 and 7
```javascript
for i in range(100):
    if i%3!=0 and i%7!=0:
        print(i)
        
    else:
        print(end="");
```

###PRINT NUMBERS WHICH ARE DIVIDED BY  2&3 FOR SPECIFIC RANGE

```javascript
for i in range(10,100):
    if i%2==0 and i%3==0:
        print(i)
    else:
        print("",end="")
 


SWAP NUMBER
a=int(input("Enter Value for a:"))
b=int(input("Enter value for b:"))

print("Value for a is  ",a,"\nValue of b is ",b)

temp=a
a=b
b=temp
print("After Swapping")
print("Value of a is ",a,"\nValue of b is  ",b)

```

### POSSITIVE OR NEGATIVE NUMBER
```javascript
num=int(input("Enter a Value "))

if num<0:
    print("Number is Negative")
elif num>0:
    print("Number is Positive")
elif num==0:
    print("Number is Zero")
    
~~~



### LEAP YEAR
```javascript
year=int(input("Enter Year:"))
if(year%4==0):
    print("Year is Leap Year")
else:
    print("Year is Not Leap Year")
```

### ARMSTRONG NUMBER

```javascript
a=int(input("Enter a Number"))
length=len(str(a))
temp=a;
sum=0;
while(a>0):
    b=a%10;
    sum=sum+b**length;
    a=a//10;
if sum==temp:
    print("Number is Armstrong number")
else:
    print("Number is not Armstrong number")
    

```

### PALLINDROME NUMBER
```javascript
a=int(input("Enter a Number:"))
temp=a;
check=0;
while(a>0):
    b=a%10;
    check=check*10+b;
    a=a//10;
if check==temp:
    print("Number is Pallindrome")
else:
    print("Number is Not Palindrome")
```

### SQUARE USING CLASS
```javascript
class square:
   
    def setvalue(self,value):
        
        
        self.value=value;
        if self.value==None:
            self.value=1;
    def getvalue(self):
        square=self.value*2;
        print("Square of number is :",+square)
        
s=square();
num=int(input("Enetr a Number"))
s.setvalue(num);
s.getvalue();
```

### EVEN AND ODD NUMBER CHECK

```javascript
num=int(input("Enter a Number:"))
if num%2==0:
    print("Number is Even")
else:
    print("Number is Odd")
```

### SUM OF EVEN NUMBER AND LOWEST ODD NUMBER
```javascript
nums=[-1,14,23,0,2,-9,19,-8,3]
sum=0;
odd=[]
for i in nums:
    
    if i%2==0:
        sum=sum+i
    else:
        odd.append(i)
print("Sum of Even Number is ",+sum)
odd.sort()
print("Lowest odd Number is.",odd[0])
```

## CLASS AND OBJECTS

## MESSAGE PASSING THROUGH CLASS
```javascript
def msg(name,messge):
    print("Hello",name,',',message)

name=input("Enter the Name:")
message=input("Enter the message:")
msg(name,message)
```
### SWAP NUMBER USING CLASS
```javascript
class swap:
    def __init__(self):
        self.a=int(input("Enter s Number. "))
        self.b=int(input("Enter s Number. "))
    def swap(self):
        a=self.a;
        b=self.b;
        a=a+b;
        b=a-b;
        a=a-b;
        return a,b
        
f=swap();
a,b=f.swap()
print("After SWapping");
print(a)
print(b)
```
### STRING PALLINDROME
```javascript
class Pallindrom:
    def checkstring(self,string):
        rev=string[::-1]
        if (rev==string):
            print("String is palindrom")
        else:
            print("string is Not Pallindrom");

string=input("Enter a String ")
s=Pallindrom();
s.checkstring(string)
```

### CALCULATER OPERATION USING CLASS
```javascript
def menu():
    print("\nEnter a operation \n1)Sum\n2)sub\n3)mul\n4)div");
    choice=int(input("Choose Operation.:"))
    return choice;

def sum(a,b):
    return a+b;
def sub(a,b):
    return a-b;
def mul(a,b):
    return a*b;
def div(a,b):
    return a//b;
a=int(input("Enter a Value "))
b=int(input("Enter a Value for b "))

c=1
while c==1:
    oper=menu();
    if oper==1:
        print("Sum of Number is ",sum(a,b));
    elif oper==2:
        print("Subtraction of Number is ",sub(a,b))
    elif oper==3:
         print("Multi of Number is ",mul(a,b))
    elif oper==4:
        print("Division is ",div(a,b))
    else:
        c=0;

 ~~~   



FILE OPERATION



TAKE NAME AND MOBILE NUMBER FROM USER AND STORE IT IN FILE

n=int(input("Enter the number of users"))
f=open("file.txt","a")
for i in range(n):
    name=str(input("Enter the Name .:"))
    mobno=input("Eneter a mobile number:")
    user=("\nUser name:")
    f.write(user)
    f.write(name)
    mob=("\nMobile No.:")
    f.write(mob)
    f.write(mobno)
f.close()
t=open("file.txt","r") 
print("Details of user\n")
for i in t: 
    
    print(t.read());
    
COPY DATA FROM ONE TO ANOTHER FILE

f=open("cont.txt",'r')
data=f.read()
    

f2=open("copy1.txt",'w')
f2.write(data)
f2.close()
f3=open("copy1.txt",'r')
print(f3.read())

SUM AND AVERAGE OF NUMBER STORE IN FILE & SEPARATED BY COMMA

def sum():
    sum=0;
    for i in l:
        k=int(i)
        sum=sum+k;
    return sum;
def avg():
    sums=sum();
    count=0;
    for i in l:
        count=count+1;
    return sums//count

f=open("Number.txt","r")
l=[]
l=f.read().split(",");
for i in l:
    print(i)
    
print("Sum of INput is ",sum())
print("Average of Input is ",avg())


FILE OPERACTION BY GIVING MENU TO THE USER

class FileManager:
    def __init__(self):
        f=open("test.txt",'a')
        f.close()
    def reads(self):
        f1=open("test.txt",'r');
        print(f1.read());
        f1.close();
        
    def writes(self):
        f2=open("test.txt",'w')
        str=input("Enter:")
        f2.write(str);
        f2.close();
        
k=FileManager();
choise=1;
while(choise>0):
    print("Choose Option:\n1)Read\n2)Write\n3)Close")
    choise=int(input())
    if(choise==1):
        k.reads();
    elif(choise==2):
        k.writes();
    elif(choise==3):
        break;
    else:
        print("!!!Enter Valide option!!!")



