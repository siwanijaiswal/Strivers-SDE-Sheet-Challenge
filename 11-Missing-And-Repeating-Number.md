 ## [Find Missing And Repeated Array](https://www.codingninjas.com/codestudio/problems/missing-and-repeating-numbers_8230733?challengeSlug=striver-sde-challenge)



```Brute force ```
 ```cpp
#include<bits/stdc++.h>
using namespace std;

vector<int> missingNrepeatedNum(vector<int> arr){
    int n= arr.size();
    int repeating = -1;
    int missing = -1;

    for(int i=1;i<=n; i++){
        int cnt =0;
        for(int j=0; j<n; j++){
            if(arr[j] == i) cnt++;
        }
        if(cnt == 2) repeating = i;
        else if(cnt == 0) missing = i;

        if(repeating != -1 & missing != -1){
            break;
        }
    }
    return {repeating, missing};
}

int main(){
    vector<int> arr;
    arr = { 3,2,2,4,1};
     vector<int> ans = missingNrepeatedNum(arr);
     cout << ans[0] <<"," << ans[1] << endl;

     return 0;
}
/*
T.C = O(N^2)
S.C = O(1)
*/
```
```Better Approach```
```cpp
#include<bits/stdc++.h>
using namespace std;

vector<int> missingNrepeatedNum(vector<int> arr){
    int n = arr.size();
    int hash[n+1] = {0};
    for(int i=0;i<n; i++){
        hash[arr[i]]++;
    }
    int repeating = -1;
    int missing = -1;

    for(int i=1;i<=n; i++){

        if(hash[i]== 2) repeating = i;
        else if(hash[i] == 0) missing = i;

        if(repeating != -1 & missing != -1){
            break;
        }
    }
    return {repeating, missing};
}
int main(){
    vector<int> arr;
    arr = { 4,3,6,2,1,1};
     vector<int> ans = missingNrepeatedNum(arr);
     cout << ans[0] <<"," << ans[1] << endl;
     return 0;
}
/*
T.C = O(2N)
S.C = O(N)
*/
```
```Optimal Approach(Mathematical)```
``` cpp
#include<bits/stdc++.h>
using namespace std;

vector<int>missingNrepeatedNum(vector<int> arr){
  long long n = arr.size();
  // S - SN = x-y
  // S2 - SN2 = x square + y square
 long long S=0, S2=0;
  long long SN = (n* (n+1))/2;
  long long SN2 = (n* (n+1)* (2*n+1))/6;

  for(int i= 0; i<n; i++){
    S += arr[i];
    S2 += (long long) arr[i] * (long long )arr[i];
  }
  long long  val1 = S - SN;
  long long  val2 = S2 - SN2;
  val2 = val2/ val1;   // x + y
  long long x = (val1 + val2)/2;
  long long y = x - val1;

  return {(int)x,(int)y};

}
int main(){
    vector<int> arr;
    arr = { 4,3,6,2,1,1};
     vector<int> ans = missingNrepeatedNum(arr);
     cout << ans[0] <<"," << ans[1] << endl;
     return 0;
}
/*
T.C = O(N)
S.C = O(1)
*/
```
