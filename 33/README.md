# Middle of the Linked List
 
Solution:
```cpp
class Solution {
public:
    ListNode* middleNode(ListNode* head) {
        ListNode* slowPointer = head;
        ListNode* fastPointer = head;

        while (fastPointer != nullptr && fastPointer->next != nullptr) {
            slowPointer = slowPointer->next;
            fastPointer = fastPointer->next->next;
        }

        return slowPointer;
    }
};
```

```
Time complexity: O(N)
Space complexity: O(1)
```