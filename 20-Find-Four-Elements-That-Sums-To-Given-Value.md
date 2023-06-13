 ## [Find Four Elements That Sums To A Given Value](https://www.codingninjas.com/codestudio/problems/find-four-elements-that-sums-to-a-given-value_8230785?challengeSlug=striver-sde-challenge)

```Optimal```
 ```cpp
 #include <bits/stdc++.h>

string fourSum(vector<int> arr, int target, int n) {
    sort(arr.begin(), arr.end());
    bool found = false;

    for (int i = 0; i < n; i++) {
        if (i > 0 && arr[i] == arr[i - 1]) continue;
        for (int j = i + 1; j < n; j++) {
            if (j != i + 1 && arr[j] == arr[j - 1]) continue;
            int k = j + 1;
            int l = n - 1;
            while (k < l) {
                long long sum = arr[i] + arr[j] + arr[k] + arr[l];
                if (sum == target) {
                    found = true;
                    break;
                }
                else if (sum < target) k++;
                else l--;
            }
            if (found) break;
        }
        if (found) break;
    }

    if (found) return "Yes";
    else return "No";

}
/*
    T.C: O(n^3)
    S.C: O(1)
    */
```

 ## [Find Four Elements That Sums To A Given Value](https://www.codingninjas.com/codestudio/problems/find-four-elements-that-sums-to-a-given-value_8230785?challengeSlug=striver-sde-challenge)

```Optimal```
 ```cpp
 #include <bits/stdc++.h>

string fourSum(vector<int> arr, int target, int n) {
    sort(arr.begin(), arr.end());
    bool found = false;

    for (int i = 0; i < n; i++) {
        if (i > 0 && arr[i] == arr[i - 1]) continue;
        for (int j = i + 1; j < n; j++) {
            if (j != i + 1 && arr[j] == arr[j - 1]) continue;
            int k = j + 1;
            int l = n - 1;
            while (k < l) {
                long long sum = arr[i] + arr[j] + arr[k] + arr[l];
                if (sum == target) {
                    found = true;
                    break;
                }
                else if (sum < target) k++;
                else l--;
            }
            if (found) break;
        }
        if (found) break;
    }

    if (found) return "Yes";
    else return "No";

}
/*
    T.C: O(n^3)
    S.C: O(1)
    */
```

