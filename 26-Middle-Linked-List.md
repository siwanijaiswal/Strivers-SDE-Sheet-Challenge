 ## [Middle of LinkedList](https://www.codingninjas.com/codestudio/problems/middle-of-linked-list_8230764?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
Node *findMiddle(Node *head) {
   if(head == NULL || head->next == NULL){
        return head;
    }

    //2 node needed or not
    if(head->next->next == NULL){
        return head->next;
    }
    Node* slow = head;
    Node* fast = head->next;
    while(fast !=NULL){
        fast = fast->next;
        if(fast != NULL){
            fast= fast->next;
        }
        slow = slow->next;
    }
    return slow;
}
// T.C = O(N)
// S.C = O(1)

``` ## [Middle of LinkedList](https://www.codingninjas.com/codestudio/problems/middle-of-linked-list_8230764?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
Node *findMiddle(Node *head) {
   if(head == NULL || head->next == NULL){
        return head;
    }

    //2 node needed or not
    if(head->next->next == NULL){
        return head->next;
    }
    Node* slow = head;
    Node* fast = head->next;
    while(fast !=NULL){
        fast = fast->next;
        if(fast != NULL){
            fast= fast->next;
        }
        slow = slow->next;
    }
    return slow;
}
// T.C = O(N)
// S.C = O(1)

```