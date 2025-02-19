Access to nested functions variable scoping
```
class Solution:
    def maxDepth(self, root: Optional[TreeNode]) -> int:
        
        result = 0

        def dfs(_root, level):
            nonlocal result
            result = max(level, result)
            if _root.left:
                dfs(_root.left, level+1)
            if _root.right:
                dfs(_root.right, level+1)

        if root:
            dfs(root, 1)

        return result
```

Python strings can't perform swapping operations.
```
# leetcode 75
class Solution:
    def reverseVowels(self, s: str) -> str:
        vowels = "aeiouAEIOU"
        s = list(s)

        # two pointers -> left right
        left, right = 0, len(s) - 1

        while left < right:
            if s[left] not in vowels:
                left += 1
                continue
            elif s[right] not in vowels:
                right -= 1
                continue
            else:
                s[left], s[right] = s[right], s[left]
                left += 1
                right -= 1
        return ''.join(s)
```






