
[Maximum Subarray Sum](https://www.codingninjas.com/codestudio/problems/maximum-subarray-sum_8230694?challengeSlug=striver-sde-challenge&leftPanelTab=1)
###(Kadane's Algorithm)

## C++:
```Optimal Approach```

```cpp
#include <bits/stdc++.h> 
long long maxSubarraySum(int arr[], int n)
{
    long long sum =0; // take initially sum as 0
    long long maxi= LONG_MIN;
    for(int i=0; i<n;i++){
        sum = sum + arr[i];
        
        if(sum < 0){  // if sum is negative , set it to 0
            sum =0;
        }
        if(sum > maxi){   //update maximum sum if sum > maxi
            maxi = sum;
        }
    }
    return maxi;
}
// T.C =O(n)
// S.C = O(1)
 
```


