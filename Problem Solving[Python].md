
# Problem-Solve



## Max-Min of Array 
#### Given N integers in array, find the minimum and maximum values that can be calculated by summing exactly N-1 of the N integers.
```javascript
def miniMaxSum(arr):
    # Write your code here
    arr.sort()
    print( sum(arr[:-1]),sum(arr[1:]))

if __name__ == '__main__':

    arr = list(map(int, input().rstrip().split()))

    miniMaxSum(arr)
```
## Number Line Jumps
#### [Que](https://www.hackerrank.com/challenges/kangaroo/problem)
```javascript
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'kangaroo' function below.
#
# The function is expected to return a STRING.
# The function accepts following parameters:
#  1. INTEGER x1
#  2. INTEGER v1
#  3. INTEGER x2
#  4. INTEGER v2
#

def kangaroo(x1, v1, x2, v2):
    # Write your code here
    n = 0;
    while (n < 10000): 
        if (x1 + n * v1 == x2 + n * v2):
            return "YES"
        
        n=n+1
    return "NO"


if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    first_multiple_input = input().rstrip().split()

    x1 = int(first_multiple_input[0])

    v1 = int(first_multiple_input[1])

    x2 = int(first_multiple_input[2])

    v2 = int(first_multiple_input[3])

    result = kangaroo(x1, v1, x2, v2)

    fptr.write(result + '\n')

    fptr.close()

```

