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
    <th colspan="2"> 섹션 00. 강좌 소개 </th>
</tr>
<tr>
    <td> 1) 강의소개 </td><td> - </td>
    <td> 2) 실전 프로젝트 예제 미리보기 </td><td> - </td>
</tr>
<tr>
    <th colspan="2"> 섹션 01. 스프링 시큐리티 기본 API 및 Filter 이해 </th>
</tr>
<tr>
    <tr><td> 1) 프로젝트 구성 및 의존성 추가 </td><td> - </td></tr>
    <tr><td> 2) 사용자 정의 보안 기능 구현 </td><td> - </td></tr>
    <tr><td> 3) Form Login 인증 </td><td> - </td></tr>
    <tr><td> 4) Form Login 인증 필터 : UsernamePasswordAuthenticationFilter </td><td> - </td></tr>
    <tr><td> 5) Logout 처리, LogoutFilter </td><td> - </td></tr>
    <tr><td> 6) Remember Me 인증 </td><td> - </td></tr>
    <tr><td> 7) Remember Me 인증 필터 : RememberMeAuthenticationFilter </td><td> - </td></tr>
    <tr><td> 8) 익명사용자 인증 필터 : AnonymousAuthenticationFilter </td><td> - </td></tr>
    <tr><td> 9) 동시 세션 제어, 세션 고정 보호, 세션 정책 </td><td> - </td></tr>
    <tr><td> 10) 세션 제어 필터 : SessionManagementFilter, ConcurrentSessionFilter </td><td> - </td></tr>
    <tr><td> 11) 권한설정과 표현식 </td><td> - </td></tr>
    <tr><td> 12) 예외 처리 및 요청 캐시 필터 : ExceptionTranslationFilter, RequestCacheAwareFilter </td><td> - </td></tr>
    <tr><td> 13) 사이트 간 요청 위조 - CSRF, CsrfFilter </td><td> - </td></tr>
</tr>
<tr>
    <th colspan="2"> 섹션 02. 스프링 시큐리티 주요 아키텍처 이해 </th>
</tr>
<tr>
    <tr><td> 1) 위임 필터 및 필터 빈 초기화 - DelegatingProxyChain, FilterChainProxy </td><td> - </td></tr>
    <tr><td> 2) 필터 초기화와 다중 보안 설정 </td><td> - </td></tr>
    <tr><td> 3) 인증 개념 이해 - Authentication </td><td> - </td></tr>
    <tr><td> 4) 인증 저장소 - SecurityContextHolder, SecurityContext </td><td> - </td></tr>
    <tr><td> 5) 인증 저장소 필터 - SecurityContextPersistenceFilter </td><td> - </td></tr>
    <tr><td> 6) 인증 흐름 이해 - Authentication Flow </td><td> - </td></tr>
    <tr><td> 7) 인증 관리자 : AuthenticationManager </td><td> - </td></tr>
    <tr><td> 8) 인증 처리자 - AuthenticationProvider </td><td> - </td></tr>
    <tr><td> 9) 인가 개념 및 필터 이해 : Authorization, FilterSecurityInterceptor </td><td> - </td></tr>
    <tr><td> 10) 인가 결정 심의자 - AccessDecisionManager, AccessDecisionVoter </td><td> - </td></tr>
    <tr><td> 11) 스프링 시큐리티 필터 및 아키텍처 정리 </td><td> - </td></tr>
</tr>
<tr>
    <th colspan="2"> 섹션 03. 실전프로젝트 -인증 프로세스 Form 인증 구현 </th>
</tr>
<tr>
    <tr><td> 1) 실전 프로젝트 생성 </td><td> - </td></tr>
    <tr><td> 2) 정적 자원 관리 - WebIgnore 설정 </td><td> - </td></tr>
    <tr><td> 3) 사용자 DB 등록 및 PasswordEncoder </td><td> - </td></tr>
    <tr><td> 4) DB 연동 인증 처리(1) : CustomUserDetailsService </td><td> - </td></tr>
    <tr><td> 5) DB 연동 인증 처리(2) : CustomAuthenticationProvider </td><td> - </td></tr>
    <tr><td> 6) 커스텀 로그인 페이지 생성하기 </td><td> - </td></tr>
    <tr><td> 7) 로그아웃 및 인증에 따른 화면 보안 처리 </td><td> - </td></tr>
    <tr><td> 8) 인증 부가 기능 - WebAuthenticationDetails, AuthenticationDetailsSource </td><td> - </td></tr>
    <tr><td> 9) 인증 성공 핸들러 : CustomAuthenticationSuccessHandler </td><td> - </td></tr>
    <tr><td> 10) 인증 실패 핸들러 : CustomAuthenticationFailureHandler </td><td> - </td></tr>
    <tr><td> 11) 인증 거부 처리 - Access Denied </td><td> - </td></tr>
</tr>
<tr>
    <th colspan="2"> 섹션 04. 실전프로젝트 - 인증 프로세스 Ajax 인증 구현 </th>
</tr>
<tr>
    <tr><td> 1) 흐름 및 개요 </td><td> - </td></tr>
    <tr><td> 2) 인증 필터 - AjaxAuthenticationFilter </td><td> - </td></tr>
    <tr><td> 3) 인증 처리자 - AjaxAuthenticationProvider </td><td> - </td></tr>
    <tr><td> 4) 인증 핸들러 - AjaxAuthenticationSuccessHandler, AjaxAuthenticationFailureHandler </td><td> - </td></tr>
    <tr><td> 5) 인증 및 인가 예외 처리 - AjaxLoginUrlAuthenticationEntryPoint, AjaxAccessDeniedHandler </td><td> - </td></tr>
    <tr><td> 6) Ajax Custom DSLs 구현하기 </td><td> - </td></tr>
    <tr><td> 7) Ajax 로그인 구현 & CSRF 설정 </td><td> - </td></tr>
</tr>
<tr>
    <th colspan="2"> 섹션 05. 실전프로젝트 - 인가 프로세스 DB 연동 웹 계층 구현</th>
</tr>
<tr>
    <tr><td> 1) 스프링 시큐리티 인가 개요 </td><td> - </td></tr>
    <tr><td> 2) 관리자 시스템 - 권한 도메인, 서비스, 리포지토리 구성 </td><td> - </td></tr>
    <tr><td> 3) 웹 기반 인가처리 DB 연동 - 주요 아키텍처 이해 </td><td> - </td></tr>
    <tr><td> 4) 웹 기반 인가처리 DB 연동 - FilterInvocationSecurityMetadataSource (1) </td><td> - </td></tr>
    <tr><td> 5) 웹 기반 인가처리 DB 연동 - FilterInvocationSecurityMetadataSource (2) </td><td> - </td></tr>
    <tr><td> 6) 웹 기반 인가처리 실시간 반영하기 </td><td> - </td></tr>
    <tr><td> 7) 인가처리 허용 필터 - PermitAllFilter 구현 </td><td> - </td></tr>
    <tr><td> 8) 계층 권한 적용하기- RoleHierarchy </td><td> - </td></tr>
    <tr><td> 9) 아이피 접속 제한하기 - CustomIpAddressVoter </td><td> - </td></tr>
</tr>
<tr>
    <th colspan="2"> 섹션 06. 실전프로젝트 - 인가 프로세스 DB 연동 서비스 계층 구현 </th>
</tr>
<tr>
    <tr><td> 1) Method 방식 개요 </td><td> - </td></tr>
    <tr><td> 2) 어노테이션 권한 설정 - @PreAuthorize, @PostAuthorize, @Secured, @RolesAllowed </td><td> - </td></tr>
    <tr><td> 3) AOP Method 기반 DB 연동 - 주요 아키텍처 이해 </td><td> - </td></tr>
    <tr><td> 4) AOP Method 기반 DB 연동 - MapBasedSecurityMetadataSource (1) </td><td> - </td></tr>
    <tr><td> 5) AOP Method 기반 DB 연동 - MapBasedSecurityMetadataSource (2) </td><td> - </td></tr>
    <tr><td> 6) AOP Method 기반 DB 연동 - MapBasedSecurityMetadataSource (3) </td><td> - </td></tr>
    <tr><td> 7) AOP Method 기반 DB 연동 - ProtectPointcutPostProcessor </td><td> - </td></tr>
</tr>
<tr>
    <th colspan="2"> 섹션 07. 번 외편 - 메소드 보안 실시간 DB 연동 구현 </th>
</tr>
<tr>
    <tr><td> ProxyFactory 를 활용한 실시간 메소드 보안 구현 </td><td> - </td></tr>
</tr>
<tr>
    <th colspan="2"> 섹션 08. 번 외편 - 강좌 마무리 </th>
</tr>
<tr>
    <tr><td> 정리 </td><td> - </td></tr>
</tr>
</table>

