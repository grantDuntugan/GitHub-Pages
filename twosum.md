# Two Sum (Python)

[<--- Head back](./index.md)

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

```
#O(n) solution

def twoSum(nums: List[int], target: int) -> List[int]:
    #Store prev computations
    m = {}
    #Iterate over list
    for i in range(len(nums)):
        #If num not in list, store indices and num to find
        if (m.setdefault(nums[i], -1) == -1):
            m[target-nums[i]] = i

        #If in list, return the indices
        else:
            return [m[nums[i]], i]
```
