1. **Brute Force Approach**
   - Time Complexity: O(n^2)
   - Space Complexity: O(log n)

'''
   class Solution {
   public:
       int findDuplicate(vector<int>& nums) {
           int repeat = 0;
           sort(nums.begin(), nums.end());
           for(int j = 0; j < nums.size(); j++) {
               for(int k = j + 1; k < nums.size(); k++) {
                   if(nums[k] == nums[j]) {
                       repeat = nums[k];
                       break;
                   }
               }
           }
           return repeat;
       }
   };
 '''

