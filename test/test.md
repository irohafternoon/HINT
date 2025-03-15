```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
 #include<map>

class Solution {
public:
    ListNode* detectCycle(ListNode* head) {
        int idx = 0;
        std::set<ListNode*> Visited_Nodes;
        ListNode* current = head;
        while (current){
            if (Visited_Nodes.contains(current)){
                return current;
            }
            Visited_Nodes.insert(current);
            current = current->next;
        }
        return NULL;
    }
};
```
aaa
