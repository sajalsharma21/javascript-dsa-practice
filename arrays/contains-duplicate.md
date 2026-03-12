# Contains Duplicate

Platform: LeetCode

## Problem

Given an integer array `nums`, return `true` if any value appears at least twice in the array, and return `false` if every element is distinct.

---

## Example

Input:

nums = [1,2,3,1]

Output:

true

Explanation:

Number `1` appears twice.

---

# Solution 1 — Brute Force (Nested Loops)

## Approach

Compare every pair of elements in the array.

If two elements are equal, it means a duplicate exists.

Time Complexity: O(n²)

## Code

```javascript
var containsDuplicate = function(nums) {

    for (let i = 0; i < nums.length; i++) {

        for (let j = i + 1; j < nums.length; j++) {

            if (nums[i] === nums[j]) {
                return true;
            }

        }

    }

    return false;

};
```

---

# Solution 2 — Optimized Approach (Using Object / Hashmap)

## Approach

Use an object to store numbers we have already seen.

While looping:
- If the number already exists in the object → duplicate found.
- Otherwise store it.

Time Complexity: O(n)

## Code

```javascript
var containsDuplicate = function(nums) {

    let seen = {};

    for (let num of nums) {

        if (seen[num]) {
            return true;
        }

        seen[num] = true;

    }

    return false;

};
```

---

## What I Learned

- How to detect duplicates in arrays
- Difference between brute force and optimized solutions
- Using objects as hashmaps in JavaScript
