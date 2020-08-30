# leetcode 121 - Best Time to Buy and Sell Stock

```C#
public static int MaxProfit(int[] prices)
{
    int minPrice = int.MaxValue;
    int maxProfit = 0;
    for(int i = 0; i < prices.Length; i++)
    {
        if (prices[i] < minPrice)
            minPrice = prices[i];
        else if (prices[i] - minPrice > maxProfit)
            maxProfit = prices[i] - minPrice;
    }
    return maxProfit;
}
```
#### Complexity Analysis
* Time Complexity: O(n)
* Space Complexity: O(1)
