# Fianal project

> 2020.06.11~2020.06.17
>
> SSAFY 1학기 마지막 프로젝트 



## 프로젝트 배경

![배경](/uploads/a468fc2784090c187e37c1ad2fb82ec1/배경.jpg)



- 영화를 본 후 영화에 대한 감상을 나누고 싶어 하는 사람들의 니즈 발견 

- 영화 정보 전달 위주의 기존 영화 사이트

- 영화 감상 공유에 초점을 둔 영화 사이트를 만들어보자!

  

## 프로젝트 목표 및 기능

![목표](/uploads/b9bc4dddad9e56f8f469a6f28c018be2/목표.jpg)

- 웹 사이트 명: **취향의 나눔**
- 대상 : 영화에 대한 감상을 자유롭게 공유하고 싶은 사람 누구나 
- 슬로건 : 당신과 닮은 취향을 가진 사람과 영화와 세계를 보는 시선을 공유해보세요.
- 목표
  - 영화 정보 조회
    - TheMovieDataBase API, Youtube API를 활용
  - 영화를 통해 자신의 취향과 개성을 표출
    - 유저 개개인에게 추천 영화 서비스 제공
    - 작성한 리뷰, 좋아하는 영화가 차곡차곡 쌓이는 개인 페이지 
    - 팔로우 기능
  - 영화 감상 공유 
    - 사용자가 감상 공유를 원하는 영화에 대해 방을 만들면 입장하여 그 영화에 대해 이야기를 나눌 수 있는 서비스 제공
    - 최근 본 영화에 대한 다른 사람들의 리뷰를 한 눈에 볼 수 있도록 UI를 구성하여 회원간 자유로운 교류 유도
    - 취향이 비슷한 유저들을 매칭해주는 서비스를 제공하고 싶었으나 시간 관계상 완성하지 못하였다. 



## 프로젝트 일정 

![일정](/uploads/0e70c4f773a77fea192dadb8dab78c57/일정.jpg)



## 팀원 및 역할 분담

팀원 : 김호연, 허예슬

공통 

- 아이디어 도출 및 기획
- 백엔드/프론트엔드(기능별로 구분)
- UCC 기획 및 제작

김호연

- 기획안, 회의록 작성 

- 회원 관리 기능 구현
  - 회원가입
  - 로그인/로그아웃
  - 프로필 페이지(팔로우/프로필 이미지 필드 등 관련 기능 구현)
- Youtube api를 활용해 예고편 기능 구현  
- 리뷰, 댓글 관련 프론트 엔드 

허예슬

- TMDB api를 활용해 영화 데이터 db 저장 
- 영화 추천 알고리즘 구현
- 영화 정보 전달 페이지, 커뮤니티 관련 백엔드 및 프론트 엔드
- 홈 페이지 관련 백엔드 및 프론트 엔드



## 페이지별 기능 및 UX 구상

![페이지별기능](/uploads/6e5288a1547b862ba2dfda6779124a97/페이지별기능.jpg)



## 데이터베이스 모델링(ERD)

![erd](/uploads/8ca62d448f3a13aabe14149ffee95df7/erd.jpg)



## 영화 추천 알고리즘

> 가장 선호하는 장르, 언어의 영화를 추천해주었다. 

1. 가장 좋아하는 장르 찾기

   - 유저가 작성한 리뷰에 대해 해당 영화가 속한 장르에 따라 평점의 평균 값을 구해준다

     ![추천1](/uploads/deeab9282d479c3a9e072cd147c79f3f/추천1.jpg)

   - 즉, 장르별 평점의 평균(총 평점/리뷰 횟수)을 구해준 후  가장 높은 평균 점수를 가진 장르를 찾는다.

     ![추천2](/uploads/c5a882e7579d626e329e1519ab217f96/추천2.jpg)

2. 가장 좋아하는 언어 찾기

   - 유저가 리뷰를 작성한 영화 중 가장 많은 언어를 찾는다. 

     ![추천3](/uploads/85d8651790b3096e6e02ec754dfa4bb8/추천3.jpg)

3. 선호하는 장르와 언어의 영화를 인기도 순으로 내림차순 한 후, 이미 본 영화를 제외하여 5개의 영화를 선택한다. 

   ![추천4](/uploads/823c49dd99e18c79c1c9dcd1b44172c0/추천4.jpg)



## 핵심기능

1. 첫 페이지

   ![템플릿](/uploads/a3acb49f4643af9daecbcdb4e696c2cd/템플릿.jpg)

   ![템플릿2](/uploads/7dbc256e599dfc0fedd497b59662e1ac/템플릿2.jpg)

   - 사이트에 대한 컨셉
   - 로그인/회원가입 

2. 홈 페이지 

   ![기능1](/uploads/0c4efc2f59bb4deac94ee18ad6be1f78/기능1.jpg)

   - 로그인한 사용자에게 영화 추천

   ![기능2](/uploads/8c776c815a6aef59e1e5149977289065/기능2.jpg)

   - 유저가 최근 작성한 리뷰에 대한 다른 사용자들의 리뷰를 한 눈에 볼 수 있게 구성

3. 개인 페이지

   ![기능3](/uploads/1e07ef12a0bcafc20ec10cf74bc000bc/기능3.jpg)

   - 프로필 이미지 등록 및 변경  
   - 팔로우 기능
   - 해당 유저가 작성한 리뷰 및 영화 조회

4. 영화 목록 페이지

   ![기능4](/uploads/5e401268d6a06c1c89c876564254893f/기능4.jpg)

   - 평점순, 최신순으로 영화 분류 및 정렬
   - 검색 기능 추가하고 싶었으나 시간 관계상 하지 못함

5. 영화 디테일 페이지

   ![기능9](/uploads/aa057d33fa91b9fb9c3a741fec99505f/기능9.jpg)

   ![기능8](/uploads/cdc262667bb80f9f51ef4031498cd07a/기능8.jpg)

   - 예고편 
   - 영화에 대한 상세 정보(평점, 개봉일, 누적 관객 등)

6. 리뷰 목록 페이지

   ![기능5](/uploads/ae9f8a7d36bf0189a0847332fbe7eb6c/기능5.jpg)

   - 감상 공유를 원하는 영화에 대한 리뷰 방을 만들 수 있다.

7. 리뷰 디테일 페이지

   ![기능6](/uploads/425eb5e424a6892b89f2a78fd1c2da3b/기능6.jpg)

   - 한 영화에 대한 유저들의 감상 조회 및 작성, 수정, 삭제 가능 

   ![기능7](/uploads/e2d8719b766b917ccfd977fab2ef3dbf/기능7.jpg)

   - 해당 리뷰에 대해 댓글 조회 및 작성, 수정, 삭제 가능 



## 느낀점

- 어려웠던 github로 협업하기 
  - 처음으로 github을 사용하여 협업해봤는데 초반에 이 기능을 사용하기까지 많은 시간이 소요됐고, 프로젝트가 끝난 지금도 github와 branch, master,,, 등등의 개념들을 완벽하게 이해하지 못하였다. 다음 프로젝트를 위해 github로 협업하는 방법에 대해 공부를 해봐야겠다.  
- 협업 시 꼭 필요한건 약속 
  - 코딩 스타일 차이에 의해 다른 사람의 코드를 이해하기 어려웠다.
  - 협업 시 네이밍 컨벤션(변수, 앱 등), 디렉토리 및 파일의 저장 위치, css 적용 방식(style 태그, 별도의 static 파일 이용) 등 세세하게 규칙을 정해야 한다는 것을 알게되었다. 
- TMDB API를 활용하여 영화 데이터 저장하기
  - 처음에는 수업시간에 많이 배웠던 ajax 요청으로 데이터를 불러오려고 했는데 매번 많은 데이터를 요청하는 것이 이상하다고 느껴져 이 방법을 포기했다.
  - 대신 python의 `requests`와 `json` 모듈을 활용하여 영화 데이터를 요청하고, 이를 json파일로 변환해준 후 `fixtures` 를 활용하여 db에 저장해주었다.
  - 이때 하드코딩으로 특정한 형태의 json 파일로 만들어주어야 db에 저장이 가능했는데, 그 이유는 알 수 없다(이 부분을 해결하기까지 많은 시간이 걸렸고 너무 힘들었다). 
  - json 데이터를 db에 저장하는 더 좋은 방법이 있을 것 같기때문에 연구해봐야겠다. 
- 소통의 필요성 
  - 사실 처음에는 취향이 같은 유저들을 매칭해주는 영화 사이트를 가장한 소개팅 서비스를 제공하고 싶었다. 그러나 취향이 같은 유저들을 찾아내는 알고리즘을 구현하기에는 시간이 부족하여 프로젝트의 방향성을 틀 수 밖에 없었다. 
  - 이러한 과정에서 팀원과 완벽하게 소통하며 같은 생각을 가지지 못했던것 같아 아쉽게 느껴진다. 프로젝트를 진행할 때 꾸준히 소통하며 서로 같은 방향을 바라볼 수 있도록 해야할 것 같다. 

- 계획은 여유있게 
  - 이틀 정도의 여유를 남기고 일정을 짜야할 것 같다. 항상 계획대로 되지 않고 마지막에 시간이 쫒기게 된다. 

