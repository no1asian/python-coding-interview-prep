
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
from collections import dequeue

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
  
  
  
