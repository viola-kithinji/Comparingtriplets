# Comparingtriplets#!/bin/python

import math
import os
import random
import re
import sys

#
# Complete the 'compareTriplets' function below.
#
# The function is expected to return an INTEGER_ARRAY.
# The function accepts following parameters:
#  1. INTEGER_ARRAY a
#  2. INTEGER_ARRAY b
#

def compareTriplets(a, b):
    pointa=0
    pointb=0
    ar=[]
    for i in range(3):
        if a[i]>b[i]:
            pointa+=1
            
        if a[i]<b[i]:
            pointb+=1
    ar.insert(0,pointa)
    ar.insert(1,pointb)
    return(ar)
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    a = map(int, raw_input().rstrip().split())

    b = map(int, raw_input().rstrip().split())

    result = compareTriplets(a, b)

    fptr.write(' '.join(map(str, result)))
    fptr.write('\n')

    fptr.close()

