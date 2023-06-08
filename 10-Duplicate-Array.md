 ## [Find Duplicate Array](https://www.codingninjas.com/codestudio/problems/find-duplicate-in-array_8230816?challengeSlug=striver-sde-challenge&leftPanelTab=1)



```Brute force / Naive approach```
 ```cpp
#include<bits/stdc++.h>
using namespace std;

int duplicateArray(vector<int> &arr){
    int n =arr.size();
    sort(arr.begin(),arr.end());

    for(int i=0; i<n; i++){
        if(arr[i] == arr[i+1]){
            return arr[i];
        }
    }
    return -1;
}
int main(){
    vector< int> arr;

    arr= {1,2,3,4,3};
    int ans = duplicateArray(arr);
    cout<< "ans is" << ans <<endl;
}
/*
T. C= O(NlogN + N)
S.C = O(1)
*/
```
```Better Approach(Hashing)/Extra Space```
 ```cpp
// extra space
#include<bits/stdc++.h>
using namespace std;

int duplicateArray(vector<int> &arr){
    int n = arr.size();
    vector<int> temp(n,0);

    for(int i=0; i<n; i++){
        if(temp[arr[i]] == 1){
            return arr[i];
        }
        temp[arr[i]] = 1;
    }
    return -1;
}
int main(){
    vector< int> arr;

    arr= {1,2,3,4,3};
    int ans = duplicateArray(arr);
    cout<< "ans is" << ans <<endl;
}
/*
T. C= O(N)
S.C = O(N)
*/
```

```Optimal Approach```
 ```cpp
#include<bits/stdc++.h>
using namespace std;

//Floyd's Tortoise and Hare Algorithm
int duplicateArray(vector<int> &arr, int n){
    // finding the point when slow and fast collide
    int slow = arr[0];
    int fast = arr[0];
    do{
        slow = arr[slow];
        fast = arr[arr[fast]];
    }
    while(slow != fast);
 
// when they collide, put fast at start point and move both by 1 pointers
    fast = arr[0];
    while(slow != fast){
        slow = arr[slow];
        fast = arr[fast];
    }
    return slow;
}
/*
T.C = O(n)
S.C = O(1)
*/
``` 



