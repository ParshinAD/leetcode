Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string "".

``` Python
class Solution:
    def longestCommonPrefix(self, strs: List[str]) -> str:
        for i in range(1, len(strs[0]) + 1):
            if not all([st[:i] == strs[0][:i] for st in strs]):
                return strs[0][:i-1]
        return strs[0]
```
