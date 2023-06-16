 ## [Merge Two Sorted Linked Lists](https://www.codingninjas.com/codestudio/problems/merge-two-sorted-linked-lists_8230729?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
Node<int>* solve(Node<int>* first, Node<int>* second){

    // if only one  element is present in first list Point its entire in second list
    if(first->next == NULL){
        first->next = second;
        return first;
    }

    Node<int>* curr1 = first;
    Node<int>* next1 = curr1->next;
    Node<int>* curr2 = second;
    Node<int>* next2 = curr2->next; 

     while(next1 != NULL && curr2 != NULL){
        if((curr2->data >= curr1->data) && (curr2->data <= next1->data)){

            // add node between first
            curr1 ->next = curr2;
            next2 = curr2->next;
            curr2->next= next1;

            //update pointers
            curr1=curr2;
            curr2 = next2;
        }
        else{
            // curr1 aur next1 ko aage badhana hai
            curr1 = next1;
            next1 = next1->next;
            if(next1 == NULL){
                curr1->next = curr2;
                return first;

            }
            
        }
     }
     return first; 
 }

Node<int>* sortTwoLists(Node<int>* first, Node<int>* second)
{
     if(first== NULL) 
    return second;

    if(second == NULL) 
    return first;

    if(first->data <= second->data){
        
       return  solve(first,second);
    }
    else{
       return  solve(second, first);
    }
}

// T.C=O(N)
// S.C =O(1)
```
