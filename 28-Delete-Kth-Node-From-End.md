 ## [Delete Kth Node From End](https://www.codingninjas.com/codestudio/problems/delete-kth-node-from-end_8230725?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
Node* removeKthNode(Node* head, int K)
{
   Node* start = new Node();
   start->next = head;
   Node* fast = start;
   Node* slow = start;

   for(int i=1; i<=K; ++i) 
   fast = fast->next;

   while(fast->next !=NULL){
       fast = fast->next;
       slow = slow->next;
   }
   slow->next = slow->next->next;
   return start->next;
}
// T.C = O(n)
// S.C = O(1)
``` ## [Delete Kth Node From End](https://www.codingninjas.com/codestudio/problems/delete-kth-node-from-end_8230725?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
Node* removeKthNode(Node* head, int K)
{
   Node* start = new Node();
   start->next = head;
   Node* fast = start;
   Node* slow = start;

   for(int i=1; i<=K; ++i) 
   fast = fast->next;

   while(fast->next !=NULL){
       fast = fast->next;
       slow = slow->next;
   }
   slow->next = slow->next->next;
   return start->next;
}
// T.C = O(n)
// S.C = O(1)
```