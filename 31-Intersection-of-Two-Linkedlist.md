 ## [Intersection of Linked List](https://www.codingninjas.com/studio/problems/intersection-of-two-linked-lists_8230688?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
Node * findIntersection(Node *firstHead, Node *secondHead)
{
    Node * a = firstHead, * b = secondHead; //two pointers

    //if a & b are not same then move them to next
    while(a != b){
        a = a ? a->next : secondHead; //if a is not null then move a to next else move it to head of second LL
        b = b ? b->next : firstHead; //if b is not null then move b to next else move it to head of first LL
    }

    return a;    
    /*
    T.C= O(n)
    S.C= O(1)
    */
}
``` 
