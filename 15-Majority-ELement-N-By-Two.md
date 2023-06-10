 ## [Majority-Element(N/2)](https://www.codingninjas.com/codestudio/problems/day-6-majority-element_8230731?challengeSlug=striver-sde-challenge&leftPanelTab=0)

```Brute force```
 ```cpp
 #include<bits/stdc++.h>
using namespace std;

int majority(int arr[], int n){
    for(int i=0; i<n; i++){
         int cnt=0;
    for(int j=0; j<n; j++){
        if(arr[i] == arr[j]) {
            cnt++;
        }
    }
    if(cnt > (n/2)) 
  return arr[i];
    }
    return -1;
}
int main(){
   int n;
   cin>>n;
   int arr[n];
   
   for(int i=0; i<n; i++){
    cin>>arr[i];
   }
   int ans = majority(arr,n);
   cout<< ans <<endl;
    return 0;
} 
// T.C = O(N^2)
// S.C = O(1)
```
```Better Approach```
```cpp
#include<bits/stdc++.h>
using namespace std;

int majority(int arr[], int n){
    //  N log n  depending on which type of map is used
   map<int ,int>mpp;
   for(int i=0; i<n; i++){
    mpp[arr[i]]++;
   }
   // o(n)
   for(auto it:mpp){
    if(it.second> (n/2)){
    return it.first;
   }
   }
   return -1;
}

int main(){
   int n;
   cin>>n;
   int arr[n];
   for(int i=0; i<n; i++){
    cin>>arr[i];
   }
   int ans = majority(arr,n);
   cout<< ans <<endl;
    return 0;
} 
// T.C = O(N logN) + O(N)
// S.C = O(N)
```
``` Optimal Approach```
``` cpp
#include <bits/stdc++.h>

int findMajorityElement(int arr[], int n) {
	 int cnt=0;
   int el;
   for(int i=0; i<n; i++){
    if(cnt ==0){
        cnt =1;
        el = arr[i];
    }
    else if(el == arr[i]){
        cnt++;
    }
    else {
        cnt--;
    }
   }
   int cnt1 =0;
   for(int i=0; i<n; i++){
    if(arr[i]== el)  cnt1++;
   }
   if(cnt1 > (n/2)){
    return el;
   }
   return -1;
} 
// T.C = O(N)
// S.C = O(1)
``` 
