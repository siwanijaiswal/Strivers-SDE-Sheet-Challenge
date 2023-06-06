 ## [Merge Overlapping Intervals](https://www.codingninjas.com/codestudio/problems/merge-intervals_8230700?challengeSlug=striver-sde-challenge&leftPanelTab=1)

```Brute Force```
```cpp
#include<bits/stdc++.h>
using namespace std;

vector<vector<int>> mergeOverlappingIntervals(vector<vector<int>> &arr){
    int n= arr.size();
    sort(arr.begin(),arr.end());
    vector<vector<int>> ans;
    for(int i=0; i<n; i++){
        int start = arr[i][0];
        int end = arr[i][1];
        if(!ans.empty() && end <= ans.back()[1]){
            continue;
        }
        for(int j=i+1; j<n; j++){
            if(arr[j][0] <=end){
                end = max(end,arr[j][1]);
            }
            else{
                break;
            }
        }
        ans.push_back({start,end});
    }
return ans;
}
// T.C = O(N logN) + O(2N)
// S.C = O(N)
```


```Optimal Approach```
 ```cpp
 #include <bits/stdc++.h> 
/*
    intervals[i][0] = start point of i'th interval
    intervals[i][1] = finish point of i'th interval
*/

vector<vector<int>> mergeIntervals(vector<vector<int>> &intervals)
{
    int n= intervals.size();
    sort(intervals.begin(),intervals.end());
    vector<vector<int>> ans;
    for(int i=0; i<n; i++){
        if(ans.empty() || intervals[i][0] > ans.back()[1]){
            ans.push_back(intervals[i]);  // adding new interval as it is greater than previous one.
        }
        else{
            ans.back()[1] = max(ans.back()[1],intervals[i][1]);
        }
    }
return ans;
}

// T.C = O(N logN) + O(N)
// S.C = O(N)
}
```
