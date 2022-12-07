- ```cpp
  class Solution {
  public:
      vector<int> sortArray(vector<int>& nums) {
          heapSort(nums);
          return nums;
      }
      void maxHeapify(vector<int>& nums, int i, int length) {
          while (2 * i + 1 < length){
              int min_index = i;
              if (2 * i + 1 < length && nums[2 * i + 1] > nums[min_index]) min_index = 2 * i + 1;
              if (2 * i + 2 < length && nums[2 * i + 2] > nums[min_index]) min_index = 2 * i + 2;
              if (min_index == i) break;
              swap(nums[min_index], nums[i]);
              i = min_index;
          }
      }
      void heapSort(vector<int>& nums) {
          for (int i = (nums.size() >> 1) - 1; i >= 0; i--) 
              maxHeapify(nums, i, nums.size());
          int end = nums.size();
          while(--end > 0) {
              swap(nums[0], nums[end]);
              maxHeapify(nums, 0, end);
          }
      }
  };
  ```