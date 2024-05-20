- info
    - lv1
    - 데이터 구조

# 이진 트리에서의 경로 합 계산
## 문제 설명
딕셔너리 형태로 주어진 이진 트리에서, 모든 루트 노드부터 리프 노드까지의 경로에 있는 노드의 값의 합을 계산하는 함수를 작성해주세요. 이진 트리는 딕셔너리로 표현되며, 각 노드는 자신의 값과 왼쪽 자식, 오른쪽 자식을 가리키는 키를 가집니다. 리프 노드는 자식이 없는 노드입니다.

예를 들어, 아래와 같은 이진 트리가 주어집니다.

```python
     1
    / \
  2   3
 / \
4  5
```

이 트리는 다음과 같은 딕셔너리로 표현될 수 있습니다: `{"value": 1, "left": {"value": 2, "left": {"value": 4}, "right": {"value": 5}}, "right": {"value": 3}}`.

루트 노드부터 리프 노드까지의 경로는 `[1, 2, 4]`, `[1, 2, 5]`, `[1, 3]`이며, 이들 경로의 합은 각각 7, 8, 4입니다.

---

## 제한 사항

- 트리의 노드 수는 1 이상 10,000 이하입니다.
- 각 노드의 값은 -10,000 이상 10,000 이하의 정수입니다.

---

## 입출력 예

|   입력 (이진 트리 딕셔너리)                       | 출력 (각 경로의 합 리스트) |
| ------------------------------------------------ | ------------------------- |
| 위 예시 트리                                     | [7, 8, 4]                 |
| {"value": 3}                                     | [3]                       |
| {"value": 1, "left": {"value": 2}, "right": {"value": 3}} | [3, 4]                   |

---

## 입출력 설명
주어진 딕셔너리 형식의 이진 트리에서 모든 루트 노드부터 리프 노드까지의 경로의 합을 계산하여 리스트로 반환합니다.