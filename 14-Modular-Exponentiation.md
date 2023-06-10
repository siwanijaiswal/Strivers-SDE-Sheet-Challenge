 ## [Modular Exponentiation](https://www.codingninjas.com/codestudio/problems/modular-exponentiation_8230803?challengeSlug=striver-sde-challenge)

```Brute force```
 ```cpp
 #include<bits/stdc++.h>
using namespace std;

int modularExponentiation(int x, int n, int m){
    long long ans = 1;
    for(int i=0; i<n; i++){
        ans  = (ans * x)%m;
    }
    return ans;
}
int main(){
    cout<< modularExponentiation(4,3,10)<<endl;
}
// T.C = O(N)
// S.C = O(1)
```
```Optimal Approach```
```cpp
#include <bits/stdc++.h>

int modularExponentiation(int x, int n, int m) {
  if(m==1) return 0;
    long long ans = 1;
    long long base = x % m;  // Take modulo of x with m
    long long nn = n;
    if (nn < 0) nn = -1 * nn;
    
    while (nn > 0) {
        if (nn % 2 == 1) {
            ans = (ans * base) % m;
        }
        base = (base * base) % m;
        nn /= 2;
    }
    
    if (n < 0) {
        ans = (ans + m) % m;
    }
    return ans;
}
// T.C = O(logn)
// S.C = O(1)
```
 
