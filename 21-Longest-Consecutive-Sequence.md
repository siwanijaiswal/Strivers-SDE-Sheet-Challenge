 ## [Longest Consecutive Sequence](https://www.codingninjas.com/codestudio/problems/longest-consecutive-sequence_8230708?challengeSlug=striver-sde-challenge&leftPanelTab=1)

```Brute Force```
 ```cpp
 #include<bits/stdc++.h>
using namespace std;

bool ls(int arr[], int n,int x){
    for(int i=0; i<n; i++){
        if(arr[i]== x ){
            return true;
        }
    }
            return false;
        }
void longest_consecutive_array(int arr[], int n){
    int x=1;
    int cnt =1;
    int mx_cnt=1;
    for(int i=0; i<n; i++){
        x=arr[i];
        cnt =1;
        while(ls(arr,n, x+1)==true)
        {
            x = x +1;
            cnt = cnt + 1;
        }
        mx_cnt = max(mx_cnt,cnt);
    }
   cout<< mx_cnt<<endl;
}

/*
    T.C: O(n^3)
    S.C: O(1)
    */
```
``` Better```
```cpp
#include<bits/stdc++.h>
using namespace std;

void longest_consecutive_array(int arr[], int n){
    int cnt =0; 
    int longest = 1;
    int last_smaller = INT_MIN;
    sort(arr, arr+n);
    if(n==0){
        cout<< 0<<endl;
    }
    for(int i=0; i<n; i++){
        if(arr[i] - 1 == last_smaller){
            cnt++;
            last_smaller = arr[i];
        }
        else if(arr[i]  != last_smaller){
            cnt =1;
            last_smaller = arr[i];
        }
        longest = max(longest, cnt);
    }
    cout<<longest <<endl; 
}
// T.C = nlogn + O(n)
// S.C =O(1)
```
``` Optimal Approach```
```cpp
#include <bits/stdc++.h>

int lengthOfLongestConsecutiveSequence(vector<int> &arr, int n) {
    int longest = 1;
    if(n==0){
        cout<< 0<<endl;
    }
    unordered_set<int>st;
    for(int i=0; i<n; i++){
        st.insert(arr[i]);
    }
  for(auto it: st){
    if(st.find(it -1) == st.end()){
        int cnt =1;
        int x = it;
        while(st.find(x+1) !=st.end()){
            x = x +1;
            cnt = cnt +1 ;
        }
        longest = max(longest,cnt);
    }
  }
    return longest;
}
// T.C = O(N)
// S.C = O(N)
   
```
