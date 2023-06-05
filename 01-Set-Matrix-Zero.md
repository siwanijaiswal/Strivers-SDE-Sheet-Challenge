

[Set Matrix Zeros](https://leetcode.com/problems/set-matrix-zeroes/description/).

## C++:

```Brute Force Approach```

```cpp
#include<bits/stdc++.h>
using namespace std;

void mark_row(vector<vector<int>> &matrix, int n, int m, int i){
 for(int j=0; j<m; j++){
    if(matrix[i][j] !=0){
        matrix[i][j] = -1;
    }
 }
}

void mark_col(vector<vector<int>> &matrix, int n, int m, int j){
 for(int i=0; i<n; i++){
    if(matrix[i][j] !=0){
        matrix[i][j]= -1;
    }
 }
}

vector<vector<int>> zeroMatrix(vector<vector<int>> &matrix, int n, int m){
    for(int i=0; i<n; i++){
        for(int j=0; j<m; j++){
            if(matrix[i][j] ==0){
                mark_row(matrix,n,m,i);
                mark_col(matrix,n,m,j);
            }
        }
    }

    for(int i=0; i<n; i++){
        for(int j=0; j<m; j++){
            if(matrix[i][j] == -1){
                matrix[i][j] = 0;

            }
        }
    }
    return matrix;
}
/*
    T.C=O(n*m)*(n+m)+(n*m) 
    */

```

```Better Approach```

```cpp
#include<bits/stdc++.h>
using namespace std;

vector<vector<int>> zeroMatrix(vector<vector<int>> &matrix,int n,int m){
    int row[n]={0};
    int col[m] ={0};

    for(int i=0; i<n; i++){
        for(int j=0; j<m; j++){
            if(matrix[i][j]==0){
               col[j] = 1;
               row[i] =1;
            }
        }
     }

    for(int i=0; i<n; i++){
        for(int j=0; j<m; j++){
            if(row[i] || col[j]){
               matrix[i][j] =0;
            }
        }
     }
     return matrix;
 
}
/*
	TC = O(n*m) + O(n*m)
	SC = O(n) + O(m)
	*/

```

```Optimal Approach```

```cpp
#include <bits/stdc++.h>

void setZeros(vector<vector<int>> &matrix)
{

  //  int col[m] ={0};  col is matrix[0][..]
  // int row[n]={0};  row is matrix[][0]
    int col0 =1;

     int n=matrix.size();
     int m=matrix[0].size();
    for(int i=0; i<n; i++){
        for(int j=0; j<m; j++){
            if(matrix[i][j]==0){
                //first i-th row
              matrix[i][0] = 0;
              //mark j-th col
              if(j != 0)
              matrix[0][j] = 0;
              else
              col0 =0;
            }
        }
     }

    for(int i=1; i<n; i++){
        for(int j=1; j<m; j++){
            if(matrix[i][j] !=0){
              //check for col and row
              if(matrix[0][j] ==0 || matrix[i][0]==0){
               matrix[i][j] = 0;
              }
            }
        }
     }
   // for col choosen , make them 0
     if(matrix[0][0] ==0){
        for(int j=0; j<m; j++) matrix[0][j] =0;
     }
      
      // for row choosen, make them 0
     if(col0== 0){
        for(int i=0; i<n; i++){
            matrix[i][0] =0;
        }
     }
}

/*
 T.C = O(n*m) + O(n*m) = O(2*n*m)
 S.C = O(1)
*/

```





## Company Tags

```Google``` ```Microsoft``` ```Netflix``` ```Meta``` ```Amazon```
