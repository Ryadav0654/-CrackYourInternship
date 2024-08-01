# Best time to buy and sell stock:

> Question link:
> https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/

> Solution link:
> https://leetcode.com/problems/best-time-to-buy-and-sell-stock/solutions/3914105/most-optimized-solution-easy-to-understand-c-java-python

### Code:

```C++
int maxProfit(vector<int>& prices) {

        int min_price = prices[0];
        int maxprof = 0;

        for(int i=1;i<prices.size();i++){
            maxprof = max(maxprof,prices[i]-min_price);
            min_price = min(prices[i],min_price);
        }

        return maxprof;

    }

```

**Time Complexity** `O(N)`, where N is the size of the prices array or vector.

**Space Complexity** `O(1)`, no extra space used.
