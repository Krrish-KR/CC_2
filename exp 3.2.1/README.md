# CC-2-exp17 (24BDA70064)
## Problem Satement: 322 Coin Change

class Solution:

    def coinChange(self, coins, amount):
        dp = [float('inf')] * (amount + 1)
        dp[0] = 0

        for x in range(1, amount + 1):
            for coin in coins:
                if x >= coin:
                    dp[x] = min(dp[x], dp[x - coin] + 1)

        return dp[amount] if dp[amount] != float('inf') else -1
