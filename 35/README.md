# Problem: Duplicate Zeros

Given a fixed-length integer array arr, duplicate each occurrence of zero, shifting the remaining elements to the right.

**Note** that elements beyond the length of the original array are not written. Do the above modifications to the input array in place and do not return anything.

Example:
```
Input: arr = [1,0,2,3,0,4,5,0]

Output: [1,0,0,2,3,0,0,4]

Explanation: After calling your function, the input array is modified to: [1,0,0,2,3,0,0,4]
```

My own solution:
```cpp
class Solution {
 public:
  vector<int>& duplicateZeros(vector<int>& arr) {
    int count = 0;
    for (auto it = arr.begin(); it < arr.end(); ++it) {
      if (*it == 0)
        count++;
      else if (count != 0) {
        for (auto it2 = arr.end() - 1; it2 >= it; --it2) {
          if(it2 + count < arr.end()) {
            *(it2 + count) = *it2;
          }
          *it2 = 0;
        }
        it += count;
        count = 0;
      }
    }
    return arr;
  }
};
```
