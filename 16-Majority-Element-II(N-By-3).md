 ## [Majority Element II](https://www.codingninjas.com/codestudio/problems/majority-element-ii_8230738?challengeSlug=striver-sde-challenge)

```Brute force```
 ```cpp
 #include <bits/stdc++.h>
using namespace std;

vector<int> majorityElement(vector<int> v) {
    int n = v.size(); 
    vector<int> ls; 
    for (int i = 0; i < n; i++) {
        // Checking if v[i] is not already
        // a part of the answer:
        if (ls.size() == 0 || ls[0] != v[i]) {
            int cnt = 0;
            for (int j = 0; j < n; j++) {
                // counting the frequency of v[i]
                if (v[j] == v[i]) {
                    cnt++;
                }
            }
            if (cnt > (n / 3))
                ls.push_back(v[i]);
        }
        if (ls.size() == 2) break;
    }=
    return ls;
}
// T.C =O(N^2)
// S.C = O(1)
```

```Better Approach```
```cpp
#include<bits/stdc++.h>
using namespace std;

vector<int>majorityelement(vector<int> v){
            vector<int>ls;
            map<int, int>mpp;
            int n= v.size();
            int mini =  (int) (n/3) + 1;

            for(int i=0; i<n; i++){
                mpp[v[i]]++;
                if(mpp[v[i]] ==  mini){
                    ls.push_back(v[i]);
                }
                if(ls.size() == 2) break;
            }
            sort(ls.begin(), ls.end());
            return ls;
} 
// T.C = O(NlogN)
// S.C = O(N)


```
``` Optimal Approach```
``` cpp
#include<bits/stdc++.h>
using namespace std;

vector<int>majorityelement(vector<int>v){
    int cnt1=0, cnt2=0;
    int el1= INT_MIN;
    int el2= INT_MIN;
    int n= v.size();

    for(int i=0; i<n; i++){
        if(cnt1 == 0 && el2 != v[i]){
            cnt1= 1;
            el1 = v[i];
        }
        else if(cnt2 ==0 && el1 != v[i]){
            cnt2 = 1;
            el2 = v[i];
        }
        else if(v[i] == el1) cnt1++;
        else if(v[i] ==el2) cnt2++;
        else{
            cnt1--;
            cnt2--;
        }
    }      
    vector<int>ls;
    cnt1=0, cnt2=0;
    for( int i=0; i<n; i++){
        if(el1 == v[i])  cnt1++;
        if(el2 == v[i]) cnt2++;
    }
    int mini = (int)(n/3) + 1;
    if(cnt1 >= mini) ls.push_back(el1);
    if(cnt2 >= mini) ls.push_back(el2);
    sort(ls.begin(), ls.end());

    return ls;
}
//T.C = O(N)
// S.C = O(1)
``` ## [Majority Element II](https://www.codingninjas.com/codestudio/problems/majority-element-ii_8230738?challengeSlug=striver-sde-challenge)

```Brute force```
 ```cpp
 #include <bits/stdc++.h>
using namespace std;

vector<int> majorityElement(vector<int> v) {
    int n = v.size(); 
    vector<int> ls; 
    for (int i = 0; i < n; i++) {
        // Checking if v[i] is not already
        // a part of the answer:
        if (ls.size() == 0 || ls[0] != v[i]) {
            int cnt = 0;
            for (int j = 0; j < n; j++) {
                // counting the frequency of v[i]
                if (v[j] == v[i]) {
                    cnt++;
                }
            }
            if (cnt > (n / 3))
                ls.push_back(v[i]);
        }
        if (ls.size() == 2) break;
    }=
    return ls;
}
// T.C =O(N^2)
// S.C = O(1)
```

```Better Approach```
```cpp
#include<bits/stdc++.h>
using namespace std;

vector<int>majorityelement(vector<int> v){
            vector<int>ls;
            map<int, int>mpp;
            int n= v.size();
            int mini =  (int) (n/3) + 1;

            for(int i=0; i<n; i++){
                mpp[v[i]]++;
                if(mpp[v[i]] ==  mini){
                    ls.push_back(v[i]);
                }
                if(ls.size() == 2) break;
            }
            sort(ls.begin(), ls.end());
            return ls;
} 
// T.C = O(NlogN)
// S.C = O(N)


```
``` Optimal Approach```
``` cpp
#include<bits/stdc++.h>
using namespace std;

vector<int>majorityelement(vector<int>v){
    int cnt1=0, cnt2=0;
    int el1= INT_MIN;
    int el2= INT_MIN;
    int n= v.size();

    for(int i=0; i<n; i++){
        if(cnt1 == 0 && el2 != v[i]){
            cnt1= 1;
            el1 = v[i];
        }
        else if(cnt2 ==0 && el1 != v[i]){
            cnt2 = 1;
            el2 = v[i];
        }
        else if(v[i] == el1) cnt1++;
        else if(v[i] ==el2) cnt2++;
        else{
            cnt1--;
            cnt2--;
        }
    }      
    vector<int>ls;
    cnt1=0, cnt2=0;
    for( int i=0; i<n; i++){
        if(el1 == v[i])  cnt1++;
        if(el2 == v[i]) cnt2++;
    }
    int mini = (int)(n/3) + 1;
    if(cnt1 >= mini) ls.push_back(el1);
    if(cnt2 >= mini) ls.push_back(el2);
    sort(ls.begin(), ls.end());

    return ls;
}
//T.C = O(N)
// S.C = O(1)
```