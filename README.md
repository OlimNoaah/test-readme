# inflearn-spring-mvc-part1
≪ 스프링 MVC 1편 | 인프런 ≫


<div align=center>
<h1> 스프링 시큐리티 - 기본편 </h1>
</div>
<div align="center">
<a href="https://www.inflearn.com/course/%EC%BD%94%EC%96%B4-%EC%8A%A4%ED%94%84%EB%A7%81-%EC%8B%9C%ED%81%90%EB%A6%AC%ED%8B%B0"> 인프런 강의 링크 </a>
</div>

<br />

## 학습내용

- 스프링 시큐리티 기본 API 사용법과 이와 관련된 Filter 이해
- 스프링 시큐리티 내부 아키텍처와 동작 방식 이해
- 실전 프로젝트를 통한 스프링 시큐리티 인증 프로세스 구현
- 실전 프로젝트를 통한 스프링 시큐리티 인가 프로세스 구현 - DB 연동을 통해 권한 제어 시스템 구현

<br />

## 목차

<table>
<tr>
    <th colspan="2"> 섹션 0. 소개 </th>
</tr>
    <tr>
        <td> 강의 소개 </td>
        <td> - </td>
    </tr>
<tr>
    <th colspan="2"> 섹션 1. 웹 애플리케이션 이해 </th>
</tr>
<tr>
    <tr>
        <td> 웹 서버, 웹 애플리케이션 서버 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 서블릿 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 동시 요청 - 멀티 쓰레드 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTML, HTTP API, CSR, SSR </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 자바 백엔드 웹 기술 역사 </td>
        <td> - </td>
    </tr>
</tr>
<tr>
    <th colspan="2"> 섹션 2. 서블릿 </th>
</tr>
<tr>
    <tr>
        <td> 프로젝트 생성 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> Hello 서블릿 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HttpServletRequest - 개요 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HttpServletRequest - 기본 사용법 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 데이터 - 개요 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 데이터 - GET 쿼리 파라미터 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 데이터 - POST HTML Form </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 데이터 - API 메시지 바디 - 단순 텍스트 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 데이터 - API 메시지 바디 - JSON </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HttpServletResponse - 기본 사용법 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 응답 데이터 - 단순 텍스트, HTML </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 응답 데이터 - API JSON </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 정리 </td>
        <td> - </td>
    </tr>
</tr>
<tr>
    <th colspan="2"> 섹션 3. 서블릿, JSP, MVC 패턴 </th>
</tr>
<tr>
    <tr>
        <td> 회원 관리 웹 애플리케이션 요구사항 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 서블릿으로 회원 관리 웹 애플리케이션 만들기 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> JSP로 회원 관리 웹 애플리케이션 만들기 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> MVC 패턴 - 개요 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> MVC 패턴 - 적용 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> MVC 패턴 - 한계 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 정리 </td>
        <td> - </td>
    </tr>
</tr>
<tr>
    <th colspan="2"> 섹션 4. MVC 프레임워크 만들기 </th>
</tr>
<tr>
    <tr>
        <td> 프론트 컨트롤러 패턴 소개 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 프론트 컨트롤러 도입 - v1 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> View 분리 - v2 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> Model 추가 - v3 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 단순하고 실용적인 컨트롤러 - v4 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 유연한 컨트롤러1 - v5 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 유연한 컨트롤러2 - v5 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 정리 </td>
        <td> - </td>
    </tr>
</tr>
<tr>
    <th colspan="2"> 섹션 5. 스프링 MVC - 구조 이해 </th>
</tr>
<tr>
    <tr>
        <td> 스프링 MVC 전체 구조 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 핸들러 매핑과 핸들러 어댑터 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 뷰 리졸버 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 스프링 MVC - 시작하기 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 스프링 MVC - 컨트롤러 통합 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 스프링 MVC - 실용적인 방식 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 정리 </td>
        <td> - </td>
    </tr>
</tr>
<tr>
    <th colspan="2"> 섹션 6. 스프링 MVC - 기본 기능 </th>
</tr>
<tr>
    <tr>
        <td> 프로젝트 생성 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 로깅 간단히 알아보기 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 요청 매핑 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 요청 매핑 - API 예시 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 - 기본, 헤더 조회 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 파라미터 - 쿼리 파라미터, HTML Form </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 파라미터 - @RequestParam </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 파라미터 - @ModelAttribute </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 메시지 - 단순 텍스트 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 요청 메시지 - JSON </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 응답 - 정적 리소스, 뷰 템플릿 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 응답 - HTTP API, 메시지 바디에 직접 입력 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> HTTP 메시지 컨버터 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 요청 매핑 헨들러 어뎁터 구조 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 정리 </td>
        <td> - </td>
    </tr>
</tr>
<tr>
    <th colspan="2"> 섹션 7. 스프링 MVC - 웹 페이지 만들기 </th>
</tr>
<tr>
    <tr>
        <td> 프로젝트 생성 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 요구사항 분석 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 상품 도메인 개발 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 상품 서비스 HTML </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 상품 목록 - 타임리프 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 상품 상세 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 상품 등록 폼 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 상품 등록 처리 - @ModelAttribute </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 상품 수정 </td>
        <td> - </td>
    </tr>
    <tr>
        <td> PRG Post/Redirect/Get </td>
        <td> - </td>
    </tr>
    <tr>
        <td> RedirectAttributes </td>
        <td> - </td>
    </tr>
    <tr>
        <td> 정리 </td>
        <td> - </td>
    </tr>
</tr>
<tr>
    <th colspan="2"> 섹션 8. 다음으로 </th>
</tr>
<tr>
    <tr>
        <td> 다음으로 </td>
        <td> - </td>
    </tr>
</tr>
</table>
