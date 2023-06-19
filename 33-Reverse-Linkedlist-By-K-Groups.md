 ## [Reverse Nodes in K-Groups](https://www.codingninjas.com/codestudio/problems/reverse-nodes-in-k-group_8230709?challengeSlug=striver-sde-challenge&leftPanelTab=0)


```cpp
#include <bits/stdc++.h>
// return head of reversed LL, next node of current node, tail of reversed LL
vector<Node*> reverseGroupOfK(Node* head,int k){
  if(!head) //if head is null
    return {NULL, NULL, NULL};

  if(!head->next) return {head,NULL,head}; //if only one node is present

  Node* temp = NULL; //to store the head of reversed LL
  Node* tail = head; //to store the tail of reversed LL
  Node* next = NULL; //to store the next node of current node

  //reverse k nodes
  for(int i = k; i>=1 and head ; i--)
  {
    next = head->next;
    head->next = temp;
    temp = head;
    head = next;
  }

  return {temp, next, tail};
}



Node *getListAfterReverseOperation(Node *head, int n, int b[]){
    if(!head || !head->next)return head;

    Node* dummy = new Node(-1);
    Node* ans = dummy;
	  Node* temp = head; //to store the head of current LL

    for(int i = 0; i < n; i++)
    {
      if(b[i] == 0){
        continue;
      }

      vector<Node*> p;
      //temp will ne null if we have reached the end of LL
      if(temp) //if temp is not null
        p = reverseGroupOfK(temp,b[i]);
      else break;

      //p has head of reversed LL at 0, next node of current node 1, tail of reversed LL 2
      dummy->next = p[0]; //head of reversed LL
      temp = p[1];
      dummy = p[2];
    }

    if(temp)dummy->next = temp;
    return ans->next;

    /*
    T.c= O(N * max(b[i])) 
    S.C= O(3)
    */
}
``` 
