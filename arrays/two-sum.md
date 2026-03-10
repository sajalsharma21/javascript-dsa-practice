# Two Sum

Platform: LeetCode

## Problem

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to the target.

You may assume that each input would have exactly one solution.

---

## Example

Input:

nums = [2,7,11,15]  
target = 9  

Output:

[0,1]

Explanation:

nums[0] + nums[1] = 2 + 7 = 9

---

## Approach

1. Loop through the array.
2. Compare every pair of numbers.
3. If the sum equals the target, return their indices.

Time Complexity: O(n²)

---

## JavaScript Code

```javascript
var twoSum = function(nums, target) {

  for (let i = 0; i < nums.length; i++) {

    for (let j = i + 1; j < nums.length; j++) {

      if (nums[i] + nums[j] === target) {
        return [i, j];
      }

    }

  }

};
```

---

## What I Learned

- Nested loops
- Array traversal
- Returning indices based on condition
