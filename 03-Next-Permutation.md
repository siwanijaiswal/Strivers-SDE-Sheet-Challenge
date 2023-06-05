
[Next Permutation](https://www.codingninjas.com/codestudio/problems/next-permutation_8230741?challengeSlug=striver-sde-challenge&leftPanelTab=1)

## C++:
```Optimal Approach```

```cpp
#include <bits/stdc++.h> 
vector<int> nextPermutation(vector<int> &permutation, int n)
{
        int ind =-1;
    for(int i=n-2; i>=0; i--){
        if(permutation[i] < permutation[i+1]){
            ind =i;
            break;
        }
    }

    if(ind==-1){
        reverse(permutation.begin(), permutation.end());
        return permutation;
    }

for(int i= n-1; i>ind; i--){
    if(permutation[i] > permutation[ind]){
        swap(permutation[i], permutation[ind]);
        break;
    }
}

reverse(permutation.begin() + ind +1, permutation.end());
return permutation;

}
// T.C = O(n)
// S.C = O(1) 
```




[Next Permutation](https://www.codingninjas.com/codestudio/problems/next-permutation_8230741?challengeSlug=striver-sde-challenge&leftPanelTab=1)

## C++:
```Optimal Approach```

```cpp
#include <bits/stdc++.h> 
vector<int> nextPermutation(vector<int> &permutation, int n)
{
        int ind =-1;
    for(int i=n-2; i>=0; i--){
        if(permutation[i] < permutation[i+1]){
            ind =i;
            break;
        }
    }

    if(ind==-1){
        reverse(permutation.begin(), permutation.end());
        return permutation;
    }

for(int i= n-1; i>ind; i--){
    if(permutation[i] > permutation[ind]){
        swap(permutation[i], permutation[ind]);
        break;
    }
}

reverse(permutation.begin() + ind +1, permutation.end());
return permutation;

}
// T.C = O(n)
// S.C = O(1) 
```



