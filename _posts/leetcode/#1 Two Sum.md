---
title: "#1 Two Sum.py"
categories:
  - LeetCode
tags:
  - Python
  - LeetCode
---

# Problem

https://leetcode.com/problems/two-sum/

# Solution

``` python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        hash_map = dict()
        for idx, num in enumerate(nums):
            if num in hash_map.keys():
                return [hash_map[num], idx]
            hash_map[target - num] = idx
```

# Result

```
Runtime: 44 ms, faster than 94.99% of Python3 online submissions for Two Sum.
Memory Usage: 15.4 MB, less than 17.99% of Python3 online submissions for Two Sum.
```
