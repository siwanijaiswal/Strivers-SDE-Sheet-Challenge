 ## [Reverse Linked List](https://www.codingninjas.com/codestudio/problems/reverse-linked-list_8230724?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
LinkedListNode<int> *reverseLinkedList(LinkedListNode<int> *head) 
{
     LinkedListNode<int> *newHead = NULL;
        while (head !=NULL){
            LinkedListNode<int> *next = head->next;
            head->next = newHead;
            newHead = head;
            head= next;
        }
        return newHead;
      } 

// T.C = O(n)
// S.C = O(1)
```
