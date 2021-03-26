# 알고리즘

-----------------------

<br />

-----------------------

### Dynamic Programming이란? 장점은?

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

피보나치를 통한 재귀와 DP 비교 설명

```python 
N = int(input())
D = [0, 1]

for i in range(2, N + 1):
    D.append(D[i-2] + D[i-1])

print(D[N])
```

</details>

-----------------------

<br />

-----------------------

### 배열 nums에 [0, n]범위의 n개의 양의 정수가 담겨있습니다. [0, n]범위 수 중에서 배열에 빠져있는 수 하나를 반환하는 가장 효율적인 알고리즘을 작성하세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

<!-- #### 문제 풀어보기: [LeetCode 268: Missing Number](https://leetcode.com/problems/missing-number/) -->

<br />

#### 풀이1. HashSet

- 알고리즘 소개
    - HashSet에 주어진 배열의 값을 넣습니다.
    - 다시 주어진 배열을 탐색하며 HashSet에 값이 있는지 찾습니다.
    - Set은 O(1)으로 찾기에 `.contatins`의 시간복잡도는 O(1)입니다.
- 알고리즘 분석 
    - 시간복잡도: O(n)
    - 공간복잡도: O(n)

```java
class Solution {
    public int missingNumber(int[] nums) {
        Set<Integer> numSet = new HashSet<Integer>();
        for (int num : nums) {
            numSet.add(num);
        }

        int expectedNumCount = nums.length + 1;
        for (int number = 0; number < expectedNumCount; number++) {
            if (!numSet.contains(number)) {
                return number;
            }
        }
        return -1;
    }
}
```

<br />

#### 풀이2. 비트 연산

- 알고리즘 소개
    - 같은 숫자를 O(1)에 지워버리는 강력한 비트 연산이 있습니다. 
    - XOR연산은 같은 수이면 0으로 바꿉니다.
    - 배열을 순회하면서 idx와 배열의 값과 XOR연산을 수행합니다.
    - 같은 수는 0으로 되므로 최종적으로 배열의 값에 누락된 수를 얻을 수 있습니다.

```
Index   0   1   2   3
Value   0   1   3   4
missing = 4^(0^0)^(1^1)^(2^3)^(3^4)  
        = (4^4)^(0^0)^(1^1)^(3^3)^2   # 교환밥칙으로 같은 수끼리 묶어준다.
        = 0^0^0^0^2                   # 같은 수 끼리 묶으면 배열에 빠진 숫자가 나오게된다.
        = 2
```

- 알고리즘 분석 
    - 시간복잡도: O(n)
    - 공간복잡도: O(1)

```java
class Solution {
    public int missingNumber(int[] nums) {
        int missing = nums.length;
        for (int i = 0; i < nums.length; i++) {
            missing ^= i ^ nums[i];
        }
        return missing;
    }
}
```

<br />

#### 풀이3. 가우스 공식

- 연속된 양의정수의 합을 구하는 공식은 다음과 같습니다. `∑​ni=​n(n+1)/2`
- `연속된 수 - 현재 배열의 수`를 빼면 배열에 누락된 한 개의 수를 구할 수 있습니다.
- 시간복잡도: O(n)
- 공간복잡도: O(1)

```java
class Solution {
    public int missingNumber(int[] nums) {
        int expectedSum = nums.length * (nums.length + 1) / 2;
        int actualSum = 0;
        for (int num : nums) {
            actualSum += num;
        }
        return expectedSum - actualSum;
    }
}
```

<br />
</details>

-----------------------

<br />

-----------------------

### map, hashmap, set에 대해서 설명하세요

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- [Link](https://gompangs.tistory.com/entry/HashMap-%EC%97%90-%EB%8C%80%ED%95%98%EC%97%AC?category=537219)

</details>

-----------------------

<br />

-----------------------

### 유전 알고리즘에 대해서 설명하세요.

> 답안 준비중입니다.

-----------------------

<br />

-----------------------

### pivotal(대각선이 고정인 행렬) 3x3, 4x4를 뒤집는 로직을 짜보세요 재귀를 써야함.

> 답안 준비중입니다.

-----------------------


<br />
<br />
<div align=center>
  <hr />
    <h3> 용감한 친구들 with 남송리 삼번지 </h3>
  <hr />
</div>
   
