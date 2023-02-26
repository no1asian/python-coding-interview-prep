
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

### Add element to the end
deq.append(0)

### Pop element from the end
deq.pop()

### Add element to the start
deq.appendleft(10)

### Pop element from the start
deq.popleft()


```

----

## Priority Queue
from queue import PriorityQueue

----------------
  
  
  
