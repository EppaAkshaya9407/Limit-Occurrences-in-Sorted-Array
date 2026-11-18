# Limit-Occurrences-in-Sorted-Array
class Solution:
    def limitOccurrences(self, nums: list[int], k: int) -> list[int]:
        if nums is None:
            return None
        count=Counter(nums)
        s=list(set(nums))
        r=[]
        for i,c in count.items():
            for j in range(min(c,k)):
                r.append(i)
        return r
        
