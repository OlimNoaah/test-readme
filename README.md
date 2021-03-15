# 데이터베이스

<br />

### 관계형 데이터베이스

- 데이터가 테이블에 저장.
	- 구성요소: 행(튜플), 열(속성)
		- 행은 순서가 없지만, 열은 순서가 있다. 
    - 스키마: 이름과 데이터 유형을 정의
	- 키: 테이블에서 특정 행을 유일하게 식별할 수 있게 하는 특징, 열 혹은 복수의 열 모음
		- 테이블의 각 행에는 프라이머리 키 값이 반드시 있어야 한다.
	- 외부키
		- 이용하여 다른 테이블과 링크할 수 있다.
		- 그 값이 다른 테이블의 키 열의 값과 같은 열
		- 참조무결성: 모든 외부 키 값이 참조하는 테이블의 값으로 존재하는 경우

<br />
<br />

### 제 1, 2, 3 정규화에 대해서 설명하세요

```

```

### ACID란?

ACID(원자성, 일관성, 고립성, 지속성)는 데이터베이스 트랜잭션이 안전하게 수행된다는 것을 보장하기 위한 성질을 가리키는 약어이다.(Wiki ACID)

트랜잭션이라는 것은 데이터베이스 내에 서 하나의 논리적 기능을 수행하기 위해 행해지는 한번에 사용도는 하나 이상의 쿼리를 모아 놓은 쪼갤 수 없는 작업의 논리적인 단위이다. 트랜젝션은 ACID를 만족해야한다. ACID는 원자성(Atomicity), 일관성(Consistency), 고립성(Isolation) 그리고 지속성(Durability)의 약자이다. 

__원자성(Atomicity)__

트랜젝션은 분해가 불가능한 최소의 단위인 하나의 원자처럼 동작한다는 의미. 트랜젝션 내의 모든 연산들은 반드시 한꺼번에 완전하게 전체가 정상적으로 수행이 완료되거나 아니면 어떠한 연산도 수행되지 않은 all or noting.

예를 들어 내가 티스토리 게시판에 글을 Post한다. 트랜잭션의 Atomicity가 보장 된다는 것은 티스토리 데이터 베이스에 성공적으로 저장되거나, 실패하거나 2가지 경우밖에 없다는 것이다. 글 내용의 절반만 저장되고 나머지는 저장안되는 경우를 없게 한다는 것이다.  

__일관성(Consistency)__
트랜잭션 작업이 시작되기 전에 데이터베이스 상태가 일관된 상태였다면 트랜잭션 작업이 종료된 후에도 일관성 있는 데이터베이스 상태를 유지해아한다.
예를 들어서 티스토리 게시판에 글을 쓰는데 제목의 글자 제한이 255자라고 하자. 트랜잭션이 일어나면 이러한 조건을 만족해야하는 것이다. 만약 이를 위반하는 트랜잭션이 있다면 거부해야한다. 

__고립성(Isolation)__
트랜잭션 작업 수행 중에는 다른 트랜잭션에 영향을 주어서도 안되고, 다른 트랜잭션들에 의해 간섭을 받아서도 안 된다는 것을 의미. 다른 트랜잭션의 영향을 받게 되면 영향을 주는 트랜잭션에 의해 자신의 동작이 달라 질 수 있기 때문에, 트랜젝션 자신은 고립된 상태에서 수행되어야 한다는 것을 의미. 즉 다수의 트랜잭션이 동시에 수행중인 상황에서 하나의 트랜잭션이 완료될 때까지는 현재 실행 중인 트랜잭션의 중간 수행결과를 다른 트랜잭션에서 보거나 참조 할 수 없다.
예를 들어서 모 커뮤니티의 자유게시판에 두 사람이 글을 거의 동시에 올린다고 하자. 그러면 두 트랜젝션에 충돌이 일어나서 User A의 제목이 저장되고 내용은 User B가 저장되는게 아니라 User A의 트랜잭션이 종료 되기 전까지 User B의 트랜젝션은 실행되지 않는 것을 말한다.

__지속성(Durablility)__
일련의 데이터 조작(트렌젝션 조작)을 완료 하고 완료 통지를 사용자가 받는 시점에서 그 조작이 영구적이 되어 그 결과를 잃지 않는 것을 나타낸다. 시스템이 정상일 때 뿐 아니라 데이터베이스나 OS의 이상 종료, 즉 시스템 장애도 견딜 수 있다는 것을 말한다. MySQL을 포함해 많은 데이터베이스의 구현에서는 트랜젝션 조작을 하드 디스크에 로그로 기록하고 시스템에 이상이 발생하면 그 로그를 사용해 이상 발생 전까지 복원하는 것으로 지속성을 실현하고 있다. 

<br />
<br />

### Index 추가의 장,단점은?

```

```

<br />
<br />

### Key에 대해서 설명하세요. 후보키, 기본키(Primary Key), 대체키(Alternate Key), 외래키(Foreign Key), 슈퍼키(Super Key) 란?

- 유일성: 릴레이션으로 입력되는 모든 튜플을 유일하게 구별할 수 있는 성질
- 최소성: 가장 적은 개수의 어트리뷰트로 구성될 수 있는 성질
이러한 특징을 가지고 있는 속성(Attribute)의 집합을 후보키라 한다.
PK는 후보키 중 설계자에 의해 선택된 한개의 키를 의미, 중복되지 않으며 NULL값을 가질 수 없다.

[종류] 
- 후보키 중 PK를 제외한 나머지 후보키는 대체키(Alternate Key)이다.
- 외래키(Foreign Key)는 각 테이블끼리 관계를 맺어줄 때 사용한다.
- 슈퍼키(Super Key)는 최소성 없이 단지 튜플을 식별하기 위해 두개 이상의 속성들의 집합으로 만들어진 키를 의미한다.

<br />
<br />

### DDL, DML, DCL에 대해서 설명하세요

```
```

<br />
<br />

### DDL, DML, DCL에 대해서 설명하세요

```
```

<br />
<br />

### 트랜잭션이란?

```

```

<br />
<br />

### ORM이란?

```

```

<br />
<br />

### NoSQL이란?

NO-SQL이란 Not Only SQL의 약자로써 기존 SQL에 비해서 특정 기능에 대해서 더 나은 기능을 제공합니다. 보통 json형태의 도큐먼트 형식으로 데이터를 저장하고 확장성이 좋기 떄문에 비정형 데이터를 다루는데 좋습니다. DB로는 대표적으로 Mongo DB가 있습니다.

<br />
<br />


### Key란? Key의 종류에 대해서 설명하세요.
+ 릴레이션에 포함된 튜플을 유일하게 구분해주는 역할을 키가 합니다. 키의 종류로는 (1)슈퍼키 (2)후보키 (3)기본키 (4)대체키 (5)외래키가 있습니다.
 
#### 키의 종류
| 고객 아이디 | 고객명 | 나이 | 직업 | 전화번호 | 
| :----------: | :---------: | :----------: | :----------: | :----------: |
|  11st  |  십일리언  |  22    |  직장인     | 010-2222-1111   |
|  coupang | 김팡맨  |   27    |  학부생   |  010-2222-3333  |
|  ebay   |  김베이  |   15    |  학부생      |  010-3333-44444  |
|  tmon |  티모니언   |  18    |  대학원생       | 010-5555-66666   |

**슈퍼키(Super Key)**
	- 유일성의 특성을 만족하는 속성 또는 속성들의 집합입니다.  
	- `직업`은 값이 같은 고객이 존재할 수 있으므로 수퍼키가 될 수 없습니다. `고객명` 또한 동명이인이 존재할 수 있으므로 슈퍼키가 될 수 없습니다. 
	- 중복 아이디 생성을 허용하지 않는 홈페이지라면 `고객 아이디` 속성은 수퍼키가 될 수 있습니다.
	- `(고객 아이디, 고객명)` 속성 집합은 수퍼키가 될 수 있습니다.
	- `(고객 아이디, 고객명)`과 같이 하나의 튜플을 구별하기 위해서 불필요한 속성의 값까지 확인할 수 있습니다. 이는 비효율적인 작업이므로 꼭 필요한 속성의 집합만을 유일하게 구분할 수 있도록 **후보키** 개념이 필요합니다.
**후보키(Candidate Key)**
    - 유일성과 최소성을 만족하는 속성 또는 속성들의 집합입니다. 최소성은 키를 구성하는 여러 속성 중에 하나라도 없으면 튜플을 유일하게 구별할 수 없는 꼭 필요한 최소한의 속성들로만 키를 구성하는 특성입니다. 
    - `고객 아이디`는 후보키가 될 수 있습니다. 
    - `(고객 아이디, 고객이름)`은 후보키가 될 수 없습니다. 왜냐하면 `고객 아이디`만으로 튜플을 유일하게 구분할 수 있기 때문입니다.
    
- **기본키(Primary Key)**
    - 릴레이션에서 튜플을 구별하기 위해 여러 개의 후보키를 사용할 필요는 없습니다. 데이터베이스 설계자는 여러 후보키 중에서 기본적으로 사용할 키를 선택하는데 이것이 **기본키**입니다.
    - **후보키**가 여러개라면 데이터베이스 사용 환경을 고려해서 적합한 것을 후보키로 사용합니다. 
    - 기본키를 정할 때 다음 두 가지를 고려해야합니다.
        + 기본키가 널 값인 튜플은 다른 튜플과 구별하여 접근하기 어려우므로 **널 값을 가질 수 있는 속성은 기본키로 부적절합니다.**  
        + 값이 자주 변경되는 속성으로 구성된 후보키를 기본키로 선택하면 값이 변경될 때마다 기본키로 적합한지 검사해야하므로 **값이 자주 변경될 수 있는 속성이 포함된 후보키는 기본키로 부적절합니다.**
        + **단순한 후보키를 기본키로 선택하세요**
          
- **대체키(Alternative Key)**
    - 기본키로 선택되지 못한 후보키들입니다. 
    - 대체키는 기본키를 대체할 수 있지만 기본키가 되지 못하고 탈락하였습니다.
    

- **외래키(Foreign Key)**
    - 어떤 릴레이션에 소속된 속성 또는 속성 집합이 다른 릴레이션의 기본키가 되는 키입니다. 
    - 다른 릴레이션이 기본키를 그대로 참조하는 속성의 집합이 외래키입니다.  
