
## List 
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
data.add(x)
data.update(x)
data.remove(x)
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
----------------
  
  
  
