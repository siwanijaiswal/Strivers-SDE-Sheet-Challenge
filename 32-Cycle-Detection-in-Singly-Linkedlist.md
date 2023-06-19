 ## [Cycle Detection in a Singly Linked List](https://www.codingninjas.com/studio/problems/cycle-detection-in-a-singly-linked-list_8230683?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Floyd's Cycle Detection Algorithm ```
```cpp
bool detectCycle(Node *head)
{
	 
    Node* slow = head;
    Node* fast = head;

    while(1){
        if(!slow || !fast || !fast->next) return false; //no cycle
        slow = slow->next;
        fast = fast ->next->next;
        if(slow == fast) return true; //cycle
    }

    
  return false;
}

// T.C = O(n)
// S.C = O(1)
``` ## [Cycle Detection in a Singly Linked List](https://www.codingninjas.com/studio/problems/cycle-detection-in-a-singly-linked-list_8230683?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Floyd's Cycle Detection Algorithm ```
```cpp
bool detectCycle(Node *head)
{
	 
    Node* slow = head;
    Node* fast = head;

    while(1){
        if(!slow || !fast || !fast->next) return false; //no cycle
        slow = slow->next;
        fast = fast ->next->next;
        if(slow == fast) return true; //cycle
    }

    
  return false;
}

// T.C = O(n)
// S.C = O(1)
```