
# Two Sum (LeetCode 1)

## Question
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

[Solution link](https://www.google.com)

## Solution (C++)
```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int,int> mp;
        for(int i=0;i<nums.size();i++){
            int diff = target - nums[i];
            if(mp.count(diff)) return {mp[diff], i};
            mp[nums[i]] = i;
        }
        return {};
    }
};
