 ## [Largest Subarray With Zero Sum](https://www.codingninjas.com/codestudio/problems/longest-subarray-zero-sum_8230747?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
#include <bits/stdc++.h>

int LongestSubsetWithZeroSum(vector < int > arr) {
  int n = arr.size();
unordered_map<int,int> mpp;
    int maxi = 0;
    int sum = 0;
    for(int i=0; i<n; i++){
        sum += arr[i];
        if(sum ==0){
            maxi = i + 1;
        }
        else{
            if(mpp.find(sum) != mpp.end()){
                maxi = max(maxi, i-mpp[sum]);
            }
            else{
                mpp[sum] = i;
            }
        }
    }
    return maxi;
}
// T.C = O(nlogn)
// S.C = O(n)
  
``` ## [Largest Subarray With Zero Sum](https://www.codingninjas.com/codestudio/problems/longest-subarray-zero-sum_8230747?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
#include <bits/stdc++.h>

int LongestSubsetWithZeroSum(vector < int > arr) {
  int n = arr.size();
unordered_map<int,int> mpp;
    int maxi = 0;
    int sum = 0;
    for(int i=0; i<n; i++){
        sum += arr[i];
        if(sum ==0){
            maxi = i + 1;
        }
        else{
            if(mpp.find(sum) != mpp.end()){
                maxi = max(maxi, i-mpp[sum]);
            }
            else{
                mpp[sum] = i;
            }
        }
    }
    return maxi;
}
// T.C = O(nlogn)
// S.C = O(n)
  
```