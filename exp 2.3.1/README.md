# CC-2-exp13 (24BDA70064)
## Problem Satement: 258. Add Digits

class Solution:

    def addDigits(self, num):
        while num >= 10:
            total = 0
            while num > 0:
                total += num % 10
                num //= 10

            num = total

        return num
