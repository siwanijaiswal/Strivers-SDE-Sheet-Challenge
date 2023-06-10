 ## [Search In a 2D Matrix](https://www.codingninjas.com/codestudio/problems/search-in-a-2d-matrix_8230773?challengeSlug=striver-sde-challenge&leftPanelTab=1)

```Brute force```
 ```cpp
 #include <bits/stdc++.h>
using namespace std;

bool searchMatrix(vector<vector<int>>& mat, int target) {
    int n = mat.size();
    int m = mat[0].size();
    for(int i = 0; i < n; i++){
        for(int j = 0; j < m; j++){
            if(mat[i][j] == target) return true;
        }
    }
    return false;
}
 /*
    TC: O(n*m)
    SC: O(1)
    */
```
```Optimal Approach```
```cpp
#include<bits/stdc++.h>
using namespace std;

bool searchMatrix(vector<vector<int>>& matrix, int target) {
        int row = matrix.size();
        int col = matrix[0].size();
        int start = 0;
        int end = row*col -1;
        int mid = start + (end - start)/2;
        
        while(start<=end){
            int element = matrix[mid/col][mid%col];
            if(element == target){
                return 1;
            }
            if(element < target){
                start= mid + 1;
            }
            else{
                end = mid -1;
            }
            mid = start + (end-start)/2;
        }
        return 0;
        
    }
   /*
    TC: O(mlogn)
    SC: O(1)
    */
```
 ## [Search In a 2D Matrix](https://www.codingninjas.com/codestudio/problems/search-in-a-2d-matrix_8230773?challengeSlug=striver-sde-challenge&leftPanelTab=1)

```Brute force```
 ```cpp
 #include <bits/stdc++.h>
using namespace std;

bool searchMatrix(vector<vector<int>>& mat, int target) {
    int n = mat.size();
    int m = mat[0].size();
    for(int i = 0; i < n; i++){
        for(int j = 0; j < m; j++){
            if(mat[i][j] == target) return true;
        }
    }
    return false;
}
 /*
    TC: O(n*m)
    SC: O(1)
    */
```
```Optimal Approach```
```cpp
#include<bits/stdc++.h>
using namespace std;

bool searchMatrix(vector<vector<int>>& matrix, int target) {
        int row = matrix.size();
        int col = matrix[0].size();
        int start = 0;
        int end = row*col -1;
        int mid = start + (end - start)/2;
        
        while(start<=end){
            int element = matrix[mid/col][mid%col];
            if(element == target){
                return 1;
            }
            if(element < target){
                start= mid + 1;
            }
            else{
                end = mid -1;
            }
            mid = start + (end-start)/2;
        }
        return 0;
        
    }
   /*
    TC: O(mlogn)
    SC: O(1)
    */
```
