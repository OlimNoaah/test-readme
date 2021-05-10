### [Java] Exception, Error의 차이에 대해서 설명하세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />
<br />

Error, Exception은 Throwable class의 subclass이지만 다음과 같은 차이가 있습니다.

<br />

<table>
<thead>
<tr>
   <td> ⠀ </td>
   <td> Error </td>
   <td> Exception </td>  
</tr>
</thead>
<tbody>
<tr>
    <tr>
      <th> 패키지 </th>
      <td> java.lang.error	 </td>
      <td> java.lang.exception </td>
   </tr>
      <th> 발생 시점 </th>
      <td> 런타임에서 발생. 컴파일 시점에서 에러가 발생할지 알 수 없다.  </td>
      <td> 
       Checked Exception은 컴파일 시점에 알 수 있다. Unchecked Exception은 런타임에서만 알 수 있다.
      </td>
   <tr>
      <th> 복구 </th>
      <td> 에러는 복구가 불가능 </td>
      <td> 
         try cactch 블락을 이용하여 복구 가능
      </td>
   </tr>
   <tr>
      <th> 타입 </th>
      <td> 모든 예외는 Unchecked Type  </td>
      <td> 
        Checked Type, Unchecked Type으로 분류
      </td>
   </tr>
   <tr>
      <th> 예시 </th>
      <td> OutOfMemory, StackOverFlow </td>
      <td> 
         Checked Exception: NoSuchMethod, ClassNotFound <br /> 
         Unchecked Exception: NullPointer, IndexOutOfBounds
      </td>
   </tr>
</tr>
</tbody>
</table>

<br />

- Checked Exception: 실행하기 전에 예측 가능한 SQLException, FileNotFoundException
- Unchecked Exception: 어플리케이션 동작시 발생하는 ArrayIndexOutOfBoundException, NullPointerException

</details>
