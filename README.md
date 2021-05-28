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


### 풀이 3. 
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
