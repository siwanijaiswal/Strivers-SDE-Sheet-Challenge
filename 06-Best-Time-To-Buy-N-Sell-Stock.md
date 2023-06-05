
[Best Time to Buy and Sell Stock](https://www.codingninjas.com/codestudio/problems/best-time-to-buy-and-sell-stock_8230746?challengeSlug=striver-sde-challenge&leftPanelTab=1)

### (Dynamic Programming)
## C++:
```Optimal Approach```

```cpp

#include <bits/stdc++.h> 
int maximumProfit(vector<int> &prices){

    int mini = prices[0];
    int maxprofit = 0;

    for(int i=0; i<prices.size(); i++){
        int cost = prices[i] - mini;
        maxprofit= max(maxprofit, cost);
        
        mini = min(mini, prices[i]);
    }
    return maxprofit;
}

// T.C = O(n)
// S.C =O(n)
 
```
