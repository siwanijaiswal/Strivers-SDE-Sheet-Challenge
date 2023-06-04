
[Pascal Triangle](https://www.codingninjas.com/codestudio/problems/pascal-s-triangle_8230805?challengeSlug=striver-sde-challenge&leftPanelTab=0)

## C++:
```Optimal Approach```

```cpp
#include <bits/stdc++.h>

vector<long long int> generateRow(int row){
    long long ans = 1;
    vector<long long int>ansRow;
    ansRow.push_back(1);
    
    for(int col=1; col<row; col++){
        ans = ans * (row - col);
        ans = ans / (col);
        ansRow.push_back(ans);
    }
    return ansRow;
}

vector<vector<long long int>> printPascal(int n) 
{
  vector<vector<long long int>> final_ans;
    for(int i=1; i<=n; i++){
        final_ans.push_back(generateRow(i));
    }
    return final_ans;
}
/*
T.C = O(N^2)
S.C = O(N^2)
*/

```




[Pascal Triangle](https://www.codingninjas.com/codestudio/problems/pascal-s-triangle_8230805?challengeSlug=striver-sde-challenge&leftPanelTab=0)

## C++:
```Optimal Approach```

```cpp
#include <bits/stdc++.h>

vector<long long int> generateRow(int row){
    long long ans = 1;
    vector<long long int>ansRow;
    ansRow.push_back(1);
    
    for(int col=1; col<row; col++){
        ans = ans * (row - col);
        ans = ans / (col);
        ansRow.push_back(ans);
    }
    return ansRow;
}

vector<vector<long long int>> printPascal(int n) 
{
  vector<vector<long long int>> final_ans;
    for(int i=1; i<=n; i++){
        final_ans.push_back(generateRow(i));
    }
    return final_ans;
}
/*
T.C = O(N^2)
S.C = O(N^2)
*/

```



