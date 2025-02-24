## useful collections modules

### Counter
- 해시 가능한 객체의 개수를 세는 데 사용되는 dict의 서브클래스
- 활용 예시: 문자열에서 문자 빈도수 계산, 리스트에서 요소 개수 세기
```
from collections import Counter

nums = [1, 2, 2, 3, 3, 3]
counter = Counter(nums)
print(counter)  # 출력: Counter({3: 3, 2: 2, 1: 1})
print(counter.most_common(1))  # 출력: [(3, 3)] (가장 많이 등장한 요소)
```

### defaultdict
- dict와 유사하지만, 키가 존재하지 않을 경우 기본값을 자동으로 생성
- 활용 예시: 리스트를 값으로 갖는 딕셔너리 생성 시 초기화 불필요
```
from collections import defaultdict

d = defaultdict(list)
d["a"].append(1)
d["b"].append(2)
print(d)  # 출력: defaultdict(<class 'list'>, {'a': [1], 'b': [2]})

```

### deque (Double-Ended Queue)
- 양쪽 끝에서 O(1) 연산으로 요소 추가 및 제거가 가능한 큐
- 활용 예시: BFS 구현, 슬라이딩 윈도우, 스택/큐 대체
```
from collections import deque

dq = deque([1, 2, 3])
dq.append(4)   # 오른쪽 추가
dq.appendleft(0)  # 왼쪽 추가
dq.pop()   # 오른쪽 제거
dq.popleft()  # 왼쪽 제거
print(dq)  # 출력: deque([1, 2, 3])

```

### OrderedDict
- 삽입 순서를 유지하는 dict
- 활용 예시: 순서가 중요한 데이터 저장 및 정렬
```
from collections import OrderedDict

od = OrderedDict()
od["a"] = 1
od["b"] = 2
od["c"] = 3
print(od)  # 출력: OrderedDict([('a', 1), ('b', 2), ('c', 3)])
```



