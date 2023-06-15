 ## [Count Subarrays with Given XOR](https://www.codingninjas.com/codestudio/problems/count-subarrays-with-given-xor_8230830?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
#include <bits/stdc++.h>

int subarraysXor(vector<int> &arr, int x)
{
    int xr = 0;
    map <int,int> mpp;
    mpp[xr] ++; //{0,1}
    int cnt =0;
    for(int i=0; i<arr.size(); i++){
        xr = xr ^ arr[i];
        // k
        int k = xr ^ x;
        cnt += mpp[k];
        mpp[xr]++;
    }
    return cnt;
}
// T.C = O(N) or O(N*logN)
// S.C = O(N)
  
``` ## [Count Subarrays with Given XOR](https://www.codingninjas.com/codestudio/problems/count-subarrays-with-given-xor_8230830?challengeSlug=striver-sde-challenge&leftPanelTab=1)

``` Optimal Approach```
```cpp
#include <bits/stdc++.h>

int subarraysXor(vector<int> &arr, int x)
{
    int xr = 0;
    map <int,int> mpp;
    mpp[xr] ++; //{0,1}
    int cnt =0;
    for(int i=0; i<arr.size(); i++){
        xr = xr ^ arr[i];
        // k
        int k = xr ^ x;
        cnt += mpp[k];
        mpp[xr]++;
    }
    return cnt;
}
// T.C = O(N) or O(N*logN)
// S.C = O(N)
  
```