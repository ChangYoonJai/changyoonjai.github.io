---
title: "#2. Add Two Numbers"
categories:
  - LeetCode
tags:
  - Python
  - LeetCode
---

## Problem

(https://leetcode.com/problems/add-two-numbers/)

## Solution

_[GitHub Link](
  https://github.com/ChangYoonJai/LeetCodeInPython/blob/master/2.%20Add%20Two%20Numbers.py
)_

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        hash_map = dict()
        for idx, num in enumerate(nums):
            if num in hash_map.keys():
                return [hash_map[num], idx]
            hash_map[target - num] = idx
```

## Result

```shell
Runtime: 68 ms, faster than 90.84% of Python3 online submissions for Add Two Numbers.
Memory Usage: 13.8 MB, less than 58.15% of Python3 online submissions for Add Two Numbers.
```
