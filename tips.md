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

