class Solution:
    def subsetXORSum(self, nums: List[int]) -> int:
        n = len(nums)
        x = 0 
        for i in range(1<<n):
            y = 0
            for j in range(n):
                if i & (1<<j):
                    y ^= nums[j]
            x += y
        return x
