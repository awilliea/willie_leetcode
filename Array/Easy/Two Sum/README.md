Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

Example:
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].

1: 暴力遍歷 O(n^2)

2: 使用Hash表，邊製作hash表的同時邊記錄與查找想找的value(因為只是兩數和，所以可以直接這樣做)
