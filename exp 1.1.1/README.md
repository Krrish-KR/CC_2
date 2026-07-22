# CC-2-exp1 (24BDA70064)
## PROBLEM STATEMENT: 219 Contains Duplicate II

class Solution:

    def containsNearbyDuplicate(self, nums, k):
        last = {}
        for i, num in enumerate(nums):
            if num in last and i - last[num] <= k:
                return True
            last[num] = i
        return False
