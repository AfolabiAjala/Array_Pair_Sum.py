# Array_Pair_Sum.py
A function that returns the number of array sum pairs in a list.

## Problem
Given an integer array, output all the unique pairs that sum up to a specific value k.

So the input:

pair_sum([1,3,2,2],4)

would return 2 pairs:

 (1,3)
 (2,2)
 
 ## Solution
 ```
 def pair_sum(arr,k):
     #check for edge cases
     if len(arr) < 2:
         return
     #create a set for tracking of numbers
     seen = set()
     output = set()
     for num in arr:
         target = k - num
     if target not in seen:
         seen.add(num)
     else:
         output.add( ((min(num,target)), max(num,target)) )
     return len(output)
 ```
