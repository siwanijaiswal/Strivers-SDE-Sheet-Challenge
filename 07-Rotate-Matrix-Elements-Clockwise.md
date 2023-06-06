 ## [Rotate Matrix Elements clockwise](https://www.codingninjas.com/codestudio/problems/rotate-matrix_8230774?challengeSlug=striver-sde-challenge&leftPanelTab=1)



 ```cpp
 #include <bits/stdc++.h>

void rotateMatrix(vector<vector<int>> &mat, int n, int m)
{
    if(n == 1 and m == 1) return;

    int top = 0, bottom = n-1, left = 0, right = m-1;

    while(top < bottom and left < right){
        int temp = mat[left][top]; 

        for(int i = top; i < bottom; i++) mat[i][left] = mat[i+1][left]; 
        for(int i = left; i < right; i++) mat[bottom][i] = mat[bottom][i+1];
        for(int i = bottom; i > top; i--) mat[i][right] = mat[i-1][right]; 
        for(int i = right; i > left+1; i--) mat[top][i] = mat[top][i-1]; 

        mat[top][left+1] = temp; 
        top++;
        bottom--;
        left++;
        right--;
    }

    /*
    TC: O(n*m)
    SC: O(1)
    */

}
```
 ## [Rotate Matrix Elements clockwise](https://www.codingninjas.com/codestudio/problems/rotate-matrix_8230774?challengeSlug=striver-sde-challenge&leftPanelTab=1)



 ```cpp
 #include <bits/stdc++.h>

void rotateMatrix(vector<vector<int>> &mat, int n, int m)
{
    if(n == 1 and m == 1) return;

    int top = 0, bottom = n-1, left = 0, right = m-1;

    while(top < bottom and left < right){
        int temp = mat[left][top]; 

        for(int i = top; i < bottom; i++) mat[i][left] = mat[i+1][left]; 
        for(int i = left; i < right; i++) mat[bottom][i] = mat[bottom][i+1];
        for(int i = bottom; i > top; i--) mat[i][right] = mat[i-1][right]; 
        for(int i = right; i > left+1; i--) mat[top][i] = mat[top][i-1]; 

        mat[top][left+1] = temp; 
        top++;
        bottom--;
        left++;
        right--;
    }

    /*
    TC: O(n*m)
    SC: O(1)
    */

}
```
