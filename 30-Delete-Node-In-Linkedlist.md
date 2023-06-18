 ## [Delete Node In A Linked List](https://www.codingninjas.com/codestudio/problems/delete-node-in-a-linked-list_8230813?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
void deleteNode(LinkedListNode<int> * node) {
    node->data = node->next->data;
    node->next= node->next->next;
}
//T.C=O(1)
//S.C=O(1)
``` 
