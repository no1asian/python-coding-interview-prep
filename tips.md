### Data class
- __init__()가 자동으로 생성됨
- __repr__()도 자동 구현됨
- 속성이 자동으로 정의됨
```
from dataclasses import dataclass

@dataclass
class Book:
    title: str
    author: str
```

### Access to nested functions variable scoping
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

### Python strings can't perform swapping operations.
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

### dataclass decoration (from Python 3.7+)
```
from dataclasses import dataclass

@dataclass
class Product:
	weight: int = None
	price: float = None
	
apple = Product()
apple.price = 0
```

### List Comprehension (generate a new list)
```
# example
[ n * 2 for n in range (1, 10+1) if n % 2 == 1]

동작 과정:
range(1, 10+1) → range(1, 11):
→ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 의 숫자들이 생성됨.
if n % 2 == 1:
→ 홀수(1, 3, 5, 7, 9)만 선택됨.
n * 2:
→ 선택된 홀수를 두 배로 만듦.
```

### Generator
```
def get_natural_number():
  n = 0
  while True:
    n += 1
    yield n
```

### Enumerate
```
a = [1, 2, 3, 4, 5]
for i, v in enumerate(a):
  print(i, v)
```

### Print
```
print('A1', 'B2')
A1 B1

print('A1', 'B2', sep=',')
A1,B2

print('A1', end=' ')
print('B1')
A1 B2

a = ['A', 'B']
print(' '.join(a))
A B
```

### Counter
```
from collections import Counter

words = ['apple', 'banana', 'apple', 'orange', 'banana']
word_counts = Counter(words)
print(word_counts)  # Output: Counter({'apple': 2, 'banana': 2, 'orange': 1})

text = "hello world"
char_counts = Counter(text)
print(char_counts)  # Output: Counter({'l': 3, 'o': 2, 'h': 1, 'e': 1, ' ': 1, 'w': 1, 'r': 1, 'd': 1})
```

### Reverse String
```
class Book:
    name: str
    id: str

    def __init__(self, name, id):
        self.name = name
        self.id = id
        
    def __str__(self):
        return f"Book: {self.name} ({self.id})"

items = [ Book("JAVA", "1011"), Book("C++", "1012"), Book("Python", "1013") ]

items.sort(key=lambda x: x.name, reverse=True)

for item in items:
    print(item.name)
```








