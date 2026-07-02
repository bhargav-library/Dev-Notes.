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
    
    
