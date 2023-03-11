
## Initialize m * n matrix
```
m, n = 3, 2
metric = [[0 for col in range(n)] for row in range(m)]
```

## List 
### methods
- append()
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
  
  
  
