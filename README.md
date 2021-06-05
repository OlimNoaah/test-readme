-----------------------

`완전탐색`, `꼬리물기 최적화`

### 배열에 빠진 수를 찾으세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

### 문제

> 서로 다른 [1, n]범위의 n-1개의 숫자가 들어있는 리스트가 주어집니다. 주어진 배열에 빠진 수를 찾으세요.

- 유사 문제: [LeetCode. Missing Number](https://leetcode.com/problems/missing-number/), [백준 1920. 수 찾기](https://www.acmicpc.net/problem/1920)

<br />

> 본 문제에 대한 상세 해설은 [covenant.tistory.com/245](https://covenant.tistory.com/245)에서 볼 수 있습니다.

<br />

### 풀이 1. 완전탐색
> 시간복잡도: O(n^2) 공간복잡도: O(1)
```python
def find_missing_number_bruteforce(A):
    N = len(A)

    for cur in range(1, N+1):
        flag = False
        for a in A:
            if cur == a:
                flag = True; break

        if flag is False:
            print("Missing number is " + str(cur))
            break
```

<br />


### 풀이 2. 정렬
> 시간복잡도: O(nlogn) 공간복잡도: O(1)

```python
def find_missing_number_sort(A):
    A.sort()
    for cur in range(1, len(A)+1):
        if cur not in A:
            print("Missing number is " + str(cur))
            break
```

<br />


### 풀이 3. 해슁
> 시간복잡도: O(n) 공간복잡도: O(n)

```python
def find_missing_number_hashing(A):
    A = set(A)

    for cur in range(1, len(A)+1):
        if cur not in A:
            print("Missing number is " + str(cur))
            break
```

<br />

### 풀이 4. 총합 공식(summation formula)
> 시간복잡도: O(n) 공간복잡도: O(1)

```python
def find_missing_number_summation_formula(A):
    N = len(A)

    total_sum = (N + 1) * N // 2
    curr_sum = sum(A)

    if total_sum - curr_sum != 0:
        print("Missing number is " + str(abs(total_sum - curr_sum)))
```

<br />

### 풀이 5. XOR
> 시간복잡도: O(n) 공간복잡도: O(1)

```python
def find_missing_number_xor(A):
    N = len(A)
    X1 = A[0]
    X2 = 1

    for i in range(0, N):
        X1 = X1 ^ A[i]
    for cur in range(1, N+2):
        X2 = X2 ^ cur

    print("Missing number is " + str(X1 ^ X2))
```

<br />
<br />
</details>
