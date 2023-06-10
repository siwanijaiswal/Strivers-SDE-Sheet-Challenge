 ## [Count Inversion](https://www.codingninjas.com/codestudio/problems/count-inversions_8230680?challengeSlug=striver-sde-challenge)



```Brute force```
 ```cpp
#include<bits/stdc++.h>
using namespace std;

int CountInversion(vector<int>& arr) {
    int n = arr.size();
    int cnt = 0;
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            if (arr[i] > arr[j]) {
                cnt += 1;
            }
        }
    }
    return cnt;
}
int main() {
    vector<int> arr = {5, 3, 2, 4, 1};
    int ans = CountInversion(arr);
    cout << ans << endl;
    return 0;
}

/*
T. C= O(N^2)
S.C = O(1)
*/
```
 ## [Count Inversion](https://www.codingninjas.com/codestudio/problems/count-inversions_8230680?challengeSlug=striver-sde-challenge)



```Brute force```
 ```cpp
#include<bits/stdc++.h>
using namespace std;

int CountInversion(vector<int>& arr) {
    int n = arr.size();
    int cnt = 0;
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            if (arr[i] > arr[j]) {
                cnt += 1;
            }
        }
    }
    return cnt;
}
int main() {
    vector<int> arr = {5, 3, 2, 4, 1};
    int ans = CountInversion(arr);
    cout << ans << endl;
    return 0;
}

/*
T. C= O(N^2)
S.C = O(1)
*/
```
