# 문화로

문화로는 뮤지컬 산업에 대한 애정을 바탕으로 커뮤니티의 증대를 위해 각종 뮤지컬에 대한 정보를 제공합니다.

<br>

## 제작 기간 & 팀원 소개
- 2021년 11월 1일 ~ 5일, 총 작업기간 5일
- 4인 1조 팀 프로젝트
  - 강태수 : https://github.com/mtae616
  - 이한샘 : https://github.com/undriedspring
  - 최수인 : https://github.com/whl5105
  - 이주형 : https://github.com/leejh4197

<br>

## 사용 기술
- python
- Flask
- MongoDB
- JQuery
- Bootstrap
- Bulma
- AWS EC2

<br>

## 와이어 프레임

피그마 :
https://www.figma.com/file/rCwFAnc5rSwEmAPZMy2mrP/%ED%95%AD%ED%95%B499?node-id=0%3A1

<br>

## 웹사이트 링크
http://taesukang.shop/

<br>

## 데모영상 유튜브 링크
https://www.youtube.com/watch?v=PckVcnKXE8A&ab_channel=%ED%95%9C%EC%83%98
<br>

## API

| 기능                  | Method  | url     | Request                        | Response |
| --------------------- | ---- | ---------- | ------------------------------ | -------- |
| 로그인                | post | /login     | { userId: id, userPw: password } | JWT token         |
| 회원가입 | post | /sign_up/save | { userId: id, userPw: pw } | |
| 게시물 리스트(메인)   | get  | / | --                             | 전체 게시글 |
| 뮤지컬 세부 정보 | get | /details | { id: id } | 세부 게시글 정보 |
| 마이페이지(후기)      | get | /myPage    | { token: mytoken }                     | 내가 작성한 리뷰 목록 |

<br>

## 직면한 문제와 해결 방안
<details>
  <summary>MVC패턴 사용 시도</summary>  
  <div markdown="1">협업을 위해 app.py를 분할해서 관리하고 싶은 관계로 기왕 하는 김에 MVC패턴을 적용해보고자 알아보았지만, 작업일정 상 기한에 맞추기 어려워 리덕스의 덕스 패턴을 참고하여 flask Blueprint 를 사용하여 페이지 단위 관리를 시행하였다. </div>
</details>
<details>
  <summary>Collection join 관련</summary>  
  <div markdown="1">이번 프로젝트를 통해 Nosql 은 처음 접해보았는데, Collection 간에 join 관련하여 lookup이라는 기능을 사용할 수 있다는 것을 찾았지만, 권장하지 않는다는 말이 지배적이라 Computed 패턴을 사용하였다. </div>
</details>
<details>
  <summary> template language 인덱싱 관련</summary>  
  <div markdown="1">데이터를 사용하면서 indexing 해야할 일이 생겼는데, template language 중 loop.index0을 활용하였다. </div>
</details>
<details>
  <summary> 사이트 레이아웃 관련</summary>  
  <div markdown="1">메인페이지 작업중 페이지 이동시 공통된 레이아웃 요소들을 표현할수 있는 방법을 고민하던 중 
flask Template Inheritance을 참고하여 레이아웃을 구조화 하였다. </div>
</details>

<br>

## 궁금한 점
- 변수명, 클래스명, 메소드명 등의 표기 방식
