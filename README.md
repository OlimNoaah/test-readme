-----------------------

`완전탐색`, `꼬리물기 최적화`

### 배열 A에서 중복되는 원소 찾는 알고리즘을 최적화해보세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


### 풀이 1. 브루트포스
> 시간복잡도: O(n^2) 공간복잡도: O(1)

```python
def bruteforce(A):
    for i in range(len(A)):
        for j in range(i + 1, len(A)):
            if A[i] == A[j]:
                print("Duplicates exist: " + str(A[i]))
                return
    print("No duplicates in given array")
```

<br />

### 풀이 2. 정렬
풀이 1을 최적화. 정렬을 하면 바로 옆의 원소와 비교하면 되기에 탐색 시간을 줄일 수 있습니다.
> 시간복잡도: O(nlogn) 공간복잡도: O(1)

```python
def sorting(A):
    A.sort()
    for i in range(len(A)-1):
        if A[i] == A[i+1]:
            print("Duplicates exist: " + str(A[i]))
            return
    print("No duplicates in given array")
```

<br />

### 풀이 3. 해쉬
`set()`에 저장하면 수를 넣기 전에 `set()`에 값이 있는지 검사할 때의 시간 복잡도는 O(1)입니다. 정렬보다 시간복잡도를 줄일 수 있습니다.
> 시간복잡도: O(n) 공간복잡도: O(n)
```python
def hash(A):
    tmp = set()
    for i in A:
        if i in tmp:
            print("Duplicates exist: " + str(i))
            return
        tmp.add(i)
    print("No duplicates in given array")
```

<br />


### 풀이 4. negation 전략
> 시간복잡도: O(n) 공간복잡도: O(1)
```python
def negation(A):
    A.sort()
    for i in range(len(A)):
        if A[abs(A[i])] < 0:
            print("Duplicates exist", abs(A[i]))
            return
        A[A[i]] = -A[A[i]]
    print("No duplicates in given array")
```

<br />
</details>

-----------------------
