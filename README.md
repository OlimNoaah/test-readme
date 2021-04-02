# 운영체제

<br />

-----------------------

### 한컴오피스 '한글'을 클릭 후 빈 화면어 커서가 깜빡이고 있다. 이때 hello world를 작성하면 컴퓨터 내부에서 어떤일이 발생하는가?

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- 키보드에서 사용자 입력이 들어오면 키보드 컨트롤러가 인터럽트를 발생시켜 CPU에게 키가 입력되었다는 사실을 알려준다.
- CPU는 현재 수행중이던 작업의 상태를 저장하고 인터럽트 요청을 처리하기 위해 OS내에 정의된 키보드 인터럽트 처리 루틴을 찾아간다.
- 키보드 인터럽트 처리 루틴은 키보드로 부터 입력받은 내용을 메모리의 특정 부분에 저장해 해당 프로그램에게 키보드 입력이 들어왔음을 알리며 인터럽트 처리를 완료한다.
- 인터럽트 처리가 끝나면 인터럽트가 발생하기 직전 상태를 복구시켜 중단되었던 작업을 재개한다.

</details>

-----------------------

<br />

-----------------------

### Process와 Thread 차이점을 설명하세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- 먼저 한가지 상황을 가정해보면 한 Server에서 같은 일을 수행하는 프로세스를 매번 fork 해서 만든다고 해보자. 이런 상황이 존재한다면 매번 동일한 코드를 복사하여 일을 수행하는 비효율적인 모습을 상상할 수 있다. fork를 하게 되면 PCB, 주소복사 등등 해줄 일이 많다. 그래서 등장한게 쓰레드인데 한 프로세스 내에서 독립적인 일을 수행해준다.
- 쓰레드는 레지스터와 스택을 제외하고는 모두 공유하여 사용하게 된다. 이렇게 될 경우 한가지 쓰레드가 I/O를 수행할 때 다른 쓰레드는 다른일을 하는 식으로 일을 좀 더 효율적으로 수행할 수 있게 된다. 그리고 요즘같이 multi-processor 환경을 갖춘 상태에서는 쓰레드로 각 CPU에 일을 할당해서 수행해 줄 수 있게 된다.

</details>

-----------------------

<br />

-----------------------

### Process와 Program 차이점을 설명하세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- 실행 상태에 있는 것을 프로세스
- 하드디스크 안에 있는 것을 프로그램

</details>

-----------------------

<br />

-----------------------

### 인터럽트에 대해서 설명하세요

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

Trap 은 S/W적으로 발생하는 인터럽트를 가리키는 명칭으로 알고있습니다. 예로 System Call, Segmentation fault 같은게 있습니다.
인터럽트는 컨트롤 씨를 누를때 처럼 H/W에서 발생하는 것을 명칭 하는 것으로 알고 있습니다.

인터럽트는 장치 내에서 예외상황이 발생하여 처리가 필요할 때 사용하는 것을 말합니다. interrupt vector에 그러한 인터럽트 신호가 오게 될 때 처리해야 하는 동작을 가리키는 주소를 적어놔 관리하게 됩니다. 무조건 우선적으로 처리되게 됩니다.


__하드웨어 인터럽트__
- 각종 하드웨어 장치들이 CPU에게 서비스를 받아야 하는 경우 발생.
- 인터럽트 라인을 통해 CPU에게 전달

__소프트웨어 인터럽트__
- 프로그램이 잘못된 연산을 수행할 경우 이에 대한 적절한 처리를 위해 사용되는 예외 상황 처리
- 자신이 작성하지 않은 코드를 운영체제로부터 서비스를 받기 위해 발생시키는 시스템콜(이를 트랩이라고 합니다.)

</details>

-----------------------

<br />

-----------------------

### DMA 존재 이유에 대해서 설명하세요

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- 모든 메모리 접근 연산이 CPU에 의해서만 이루어질 경우 주변 장치가 메모리 접근을 원할 때마다 인터럽트를 통해 CPU 업무가 방해를 받게 되어 CPU의 사용의 효율성이 떨어지는 문제가 발생한다. 
- DMA는 일종의 컨트롤러로서 CPU가 주변 장치들의 메모리 접근 요청에 의해 자주 인터럽트당하는 것을 막아주는 역할을 한다.
- DMA를 사용하면 로컬 버퍼에서 메모리로 읽어오는 작업을 CPU가 담당하는 것이 아니라, DMA가 대행하므로서 CPU는 원래 하던 작업을 멈추고 인터럽트를 처리할 필요가 없어지는 것이다. 

</details>

-----------------------

<br />

-----------------------

### 운영체제는 다중 유저가 하나의 컴퓨터의 자원을 사용할 때 자원의 '보호'를 합니다. 어떠한 보호를 하는지 설명하고 시나리오를 설명하세요

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

크게 세 부분으로 나눌 수 있습니다.

__[1] 입출력장치 보호__
- A가 프린터에 인쇄를 요청하여 프린터가 A의 작업을 수행 중일 때 B가 프린터 요청을 하면 A의 작업 이후에 B의  작업을 수행해야합니다.
- 이와 관계된특권 명령(in, out) 명령은 에플리케이션에서 하는 것이 아닌 운영체제가 수행합니다. 

__[2] 메모리 보호__
- A가 실행한 프로세스는 B가 실행한 프로세스의 메모리를 읽거나 쓰지 못하도록 막습니다.
- CPU와 메모리 사이에 MMU(Memory Management Unit)두어서  base, limit 레지스터 값을 읽어서 해당 메모리 부분을 넘지 못하도록 합니다. 

__[3] CPU 보호__
- while ( n = 1) 과 같이 실수 혹은 고의로  하나의 프로세스가 CPU시간을 독점하는 일을 방지해야합니다.
- 일정 주기로 CPU에게 타이머가 인터럽트를 걸도록 회로를 설계합니다. 인터럽트를 걸면 CPU는 지금 하는 일을 멈추고 인터럽트 서비스 루틴으로 넘어갑니다. 이 코드에는 CPU 시간이 다른 모든 프로세스에게 골고루 가는지, 한 놈에게 집중되는지 체크합니다.

</details>

-----------------------

<br />

-----------------------

### synchronized에 대해 아는 바를 전부 이야기하세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

Topic
- 멀티스레딩 상황의 제어를 위해 synchronized를 적극 활용.
- 어떤 멀티스레드 상황이었는지, 왜 synchronized를 썼는지, synchronized가 mutex를 어떻게 보장하는지
- 내부적으로 어떻게 구현했는지, 다른 방법은 없었는지, 다른 방법과 synchronized를 비교했을 때의 장단점은 무엇인지, 
- 특정 상황을 제시한 뒤 이 경우라면 어떻게 적용시킬 수 있을 것인지

</details>

-----------------------

<br />

-----------------------

### 함수호출과 시스템 콜의 차이에 대해서 설명하세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- 함수호출 : 자신이 작성한 함수 혹은 라이브러리에 저장된 함수를 호출하는 것
- 시스템 콜 : 운영체제에 정의된 함수를 호출하는 것

</details>

-----------------------

<br />

-----------------------

### 인터럽트와 시스템 콜의 차이에 대해서 설명하세요.

<details>
   <summary> 읽기자료 보기 (👈 Click)</summary>
<br />

- [Leetcode](https://leetcode.com/discuss/interview-question/operating-system/124838/Interrupt-Vs-System-Call)
- [Topcoder](https://accounts.topcoder.com/member?retUrl=https:%2F%2Fwww.topcoder.com%2Fsettings%2Fprofile&utm_source=community-app-main)

</details>

-----------------------

<br />

-----------------------

### Virtual Memory에 대해서 설명하시고 사용했을 때 장점에 대해서 설명하세요.

> 답안 준비중입니다.

-----------------------

<br />

-----------------------

### Page Fault를 줄이는 방법에 대해서 설명하세요

> 답안 준비중입니다.

<br />

-----------------------

### OS에서 프로세스는 CPU와 메모리 사이에 MMU(Memory Management Unit)를 두어서 다른 프로세스에 접근할하지 못합니다. 그러나 GDB와 같은 디버거의 경우 다른 프로세스에 접근하여 절대적 메모리 주소와 값을 읽어올 수 있습니다. 어떻게 가능한지 동작 방식에 대해서 설명하세요.

> 답안 준비중입니다.

-----------------------

<br />

### 이중모드의 특징과 장점에 대해 설명하세요

> 답안 준비중입니다.

-----------------------

<br />

-----------------------

### 임계구역 문제가 무엇이고 어떻게 해결하는지 설명하시오

> 답안 준비중입니다.

-----------------------

<br />

### System Call에 대해서 설명하세요

> 답안 준비중입니다.

-----------------------

<br />

-----------------------

### 64비트와 32비트 차이는 무엇인가요? 

> 답안 준비중입니다.

-----------------------

<br />

-----------------------

### 마우스로 한글 바로가기를 클릭했을 때 컴퓨터에서 일어나는 모든 일에 대해서 설명하세요.

`Points: Interrupt, Process Scheduling, Disk Scheduling, Swapping, Thread`

> 답안 준비중입니다.

<br />
<br />
<div align=center>
  <hr />
    <h3> 용감한 친구들 with 남송리 삼번지 </h3>
  <hr />
</div>
   
