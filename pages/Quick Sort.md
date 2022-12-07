- ```cpp
  class Solution {
  public:
      void quickSort(vector<int>& nums, int lo, int hi) {
          if (lo >= hi) return;
          int left = lo - 1, right = hi + 1;
          int mid = nums[(hi + lo) >> 1];
          while (true) {
              while (nums[++left] < mid);
              while (nums[--right] > mid);
              if (left >= right) {
                  quickSort(nums, lo, right);
                  quickSort(nums, right + 1, hi);
                  return;
              }
              swap(nums[left], nums[right]);
          }
      }
      vector<int> sortArray(vector<int>& nums) {
          quickSort(nums, 0, nums.size() - 1);
          return nums;
      }
  };	
  ```