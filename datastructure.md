
## Initialize m * n matrix
```
m, n = 3, 2
metric = [[0 for col in range(n)] for row in range(m)]
```

## List 
### methods
- append()
- pop()   # pop() -> O(1), pop(0) -> O(n) Use deque
- sort(), sort(reverse=True)
- reverse()
- extend()    # adds the specified list elements (or any iterable) to the end of the current list
- insert()
- count()
- remove()
```
data = list()

# Add item
data.append(x)

# Remove last item
data.pop()

# Remove first item
data.pop(0)

data.sort()
data.reverse()
data.count(x)
```


## Dict 
```
data = dict()
data.keys()
data.values()
data.items()
data.get(x)
data.clear()

x in data 
```

## Set
```
data = set()
data = {}
data.add(x)
data.update(x)
data.remove(x)
```

## tuple
```
data = tuple()
data = ()
```

## Data Class

```
from dataclasses import dataclass

@dataclass
class Product:
  width: int = None
  height: int = None
  
sample = Product()
sample.width = 100
```

## Dequeue
```
from collections import deque

deq = deque()

# Add element to the end
deq.append(4)

# Pop element from the start
deq.popleft()

# Pop element from the end
deq.pop()

# Add element to the start
deq.appendleft()

# Reverse
deq.reverse()
```

----

## Priority Queue
```
from queue import PriorityQueue
que = PriorityQueue()
que.put(4)
que.put(1)
que.get()
que.get()
```

---

## Heap
```
import heapq
h = []
heapq.heappush(h, value)
heapq.heappop(h)

```

---
# collections

## defaultdict
```
from collections import

# 기본값이 0인 정수 사전 생성
int_dict = defaultdict(int)

# 값을 추가하지 않았는데도 기본값이 0으로 설정됨
print(int_dict["a"])  # 출력: 0

# 값 추가
int_dict["a"] += 1
print(int_dict["a"])  # 출력: 1

# 기본값이 빈 리스트인 사전 생성
list_dict = defaultdict(list)

# 값 추가
list_dict["fruits"].append("apple")
list_dict["fruits"].append("banana")

print(list_dict["fruits"])  # 출력: ['apple', 'banana']

# 값이 없는 키 접근 시, 기본값으로 빈 리스트가 설정됨
print(list_dict["vegetables"])  # 출력: []

```

## Counter
most_common()
total()
elements()
```
from collections import Counter
Counter(["hi", "hey", "hi", "hi", "hello", "hey"])
Counter({'hi': 3, 'hey': 2, 'hello': 1})

Counter("hello world")
Counter({'h': 1, 'e': 1, 'l': 3, 'o': 2, ' ': 1, 'w': 1, 'r': 1, 'd': 1})

Counter('hello world').most_common()

```

----------------
  
  
  
