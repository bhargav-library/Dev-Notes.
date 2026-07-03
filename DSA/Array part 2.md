1. Given an integer array nums, move all 0’s to the end of it while maintaining the relative order of the non-zero elements.

Note:You must do this in-place without making a copy of the array.


Example 1:

Input:nums = [0,1,0,3,12]

Output:[1,3,12,0,0]

solution:

var moveZeroes = function(nums) {

      let x = 0;
      
      for (let i = 0; i < nums.length; i++)
      {
          if (nums[i] !== 0) {
          
              nums[x] = nums[i];
              
              x++;
          }
      }
      
      for (let i = x; i < nums.length; i++) {
      
          nums[i] = 0;
          
      }
      
  };


    Problem Statement:
You are given two integer arrays nums1 and nums2, sorted in non-decreasing order, and two integers m and n, representing the number of elements in nums1 and nums2 respectively.

Mergenums1 and nums2 into a single array sorted in non-decreasing order.

The final sorted array should not be returned by the function, but instead be stored inside the array nums1. To accommodate this, nums1 has a length of m + n, where the first m elements denote the elements that should be merged, and the last n elements are set to 0 and should be ignored. nums2 has a length of n.

Examples:
Example 1:
Input:

nums1 = [1,2,3,0,0,0], m = 3 nums2 = [2,5,6], n = 3

Output: [1,2,2,3,5,6]
    
