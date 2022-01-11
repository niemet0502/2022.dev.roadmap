## 169. Majority Element [Easy]

Given an array nums of size n, return the majority element.

The majority element is the element that appears more than ⌊n / 2⌋ times. You may assume that the majority element always exists in the array.

_Example 1:_

```
Input: nums = [3,2,3]
Output: 3
```

_Example 2:_

```
Input: nums = [2,2,1,1,1,2,2]
Output: 2
```

Here my solution

```
let majorityCount = 0;
  let majority = 0;
  for (var i = 0; i < nums.length; i++) {
    let count = 0;
    for (var j = i; j < nums.length; j++) {
      if (nums[i] == nums[j]) {
        count++;
      }
    }

    if (count > nums.length / 2 && count > majorityCount) {
      majorityCount = count;
      majority = nums[i];
    }
  }

  return majority;

```
