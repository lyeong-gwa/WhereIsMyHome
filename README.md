# WhereIsMyHome
부동산데이터 및 주변상권데이터를 활용한 부동산서비스 프로젝트

## 1. 기술 스택
<img src="https://img.shields.io/badge/HTML5-E34F26?style=plastic&logo=HTML5&logoColor=white"/> <img src="https://img.shields.io/badge/CSS3-1572B6?style=plastic&logo=CSS3&logoColor=white"/> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=plastic&logo=JavaScript&logoColor=white"/> <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=plastic&logo=Vue.js&logoColor=white"/> <img src="https://img.shields.io/badge/Vuetify-1867C0?style=plastic&logo=Vuetify&logoColor=white"/> 
<p>
<img src="https://img.shields.io/badge/Java-007396?style=plastic&logo=Java&logoColor=white"/> <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=plastic&logo=Spring%20Boot&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=plastic&logo=MySQL&logoColor=white"/>
<p>
<img src="https://img.shields.io/badge/GitHub-181717?style=plastic&logo=GitHub&logoColor=white"/>
<img src="https://img.shields.io/badge/Visual%20Studio%20Code-007ACC?style=plastic&logo=Visual%20Studio%20Code&logoColor=white"/>

## 2. 주요기능 (:white_check_mark: = 맡은역할 )
* :white_large_square: 공지사항
* :white_check_mark: QnA 게시판 
* :white_large_square: JWT 로그인 
* :white_check_mark: 소셜 로그인 (Kakao API 활용)
* :white_check_mark: 부동산 정보 및 서비스 (공공 API활용,kakao Map 활용)

## 3. 설계
* 아키텍처 <p>
  ![image](https://user-images.githubusercontent.com/75747197/210081322-cfc57a10-586e-42d7-9b46-ad7db43ca24a.png)
* Usecase Diagram <p>
![image](https://user-images.githubusercontent.com/75747197/210095983-60c9e00d-17a4-497a-a5c7-0be8e83863ec.png)

* Rest API <p>
  |Method|URL|설명 |
  |----|----|----|
  |부동산 API|
  |GET|/rest/house/interest|로그인된 사용자가 선택한 관심지역 데이터 제공|
  |GET|/rest/house/search/housedeal/{aptCode}|aptCode에 해당하는 아파트거래 정보 제공|
  |POST|/rest/house/interest|로그인된 사용자의 관심지역 리스트에 관심지역을 추가|
  |POST|/rest/house/search/dongList|요청한 동들의 모든 아파트 정보들을 제공|
  |DELETE|/rest/house/interest/{aptCode}|로그인된 사용자의 관심지역 리스트에서 <p>aptCode에 해당하는 아파트를 제거|
  |GET|/rest/area|검색하고자 하는 시 데이터 제공|
  |GET|/rest/area/{sidoName}|sidoName에 속한 구군 데이터 제공|
  |GET|/rest/area/{sidoName/{gugunName}}|sidoName과 gugunName에 속한 동 데이터 제공|
  |공지사항 API|
  |GET|/rest/notice/article/{no}|공지사항 식별값(no)에 해당하는 공지사항 정보 불러오기|
  |DELETE|/rest/notice/delete/{no}|no에 해당하는 공지사항 제거|
  |GET|/rest/notice/list|공지사항 리스트 불러오기|
  |PUT|/rest/notice/modify|공지사항 글 수정|
  |GET|/rest/notice/search/{title}|공지사항 제목 키워드를 사용해서 공지사항 정보 불러오기|
  |POST|/rest/notice/write|공지사항 글 추가|
  |QnA API|
  |GET|/rest/qna/question|모든 질문데이터 리스트로 제공|
  |GET|/rest/qna/question/{no}|no에 해당하는 질문글 데이터 제공|
  |POST|/rest/qna/question/write|질문글 작성|
  |PUT|/rest/qna/question/modify|질문글 수정|
  |PUT|/rest/qna/question/complete/{questionno}|questionno에 해당하는 질문글의 답변완료 여부상태를 변경|
  |DELETE|/rest/qna/question/delete/{questionno}|questionno에 해당하는 질문글을 삭제|
  |GET|/rest/qna/answer/{questionno}|questionno에 해당하는 질문과 관련한 답변(댓글)들 제공|
  |DELETE|/rest/qna/answer/delete/{answerno}|answerno에 해당하는 답변(댓글)을 제거|
  |PUT|/rest/qna/answer/modify|QnA에 달린 답변(댓글)을 수정|
  |POST|/rest/qna/answer/write|QnA에 답변(댓글)작성|
  |로그인 API|
  |GET|/rest/user/info/{memberid}|memberid에 해당하는 사용자의 정보를 제공|
  |POST|/rest/user/findpwd|사용자 비밀번호 찾을 때 사용|
  |POST|/rest/user/join|작성한 정보들을 받아 사용자 추가(회원가입)|
  |POST|/rest/user/kakao|kakao 소셜 로그인할 때 요청|
  |POST|/rest/user/login|로그인 확인|
  |GET|/rest/user/logout/{memberid}|사용자 로그아웃|
  |PUT|/rest/user/modify|사용자 정보 수정|
  |POST|/rest/user/refresh|JWT refresh 요청|
  |PUT|/rest/user/updatepwd|사용자 비밀번호 재설정에 사용|
  |DELETE|/rest/user/delete/{memberid}|사용자 회원탈퇴|
  

## 4. 리뷰
* 프로젝트 설계에 맞게 다양한 기능을 구현하고 기능들을 유기적으로 연결하는 과정에서 명확한 설계의 중요성을 알 수 있었습니다.
* SSAFY 교육과정에서 배운 내용을 실제로 개발에 사용함으로서 알고있는 지식에 대한 이해도를 높일 수 있었습니다.
* 특히 Java Spring의 MVC패턴과 Vue의 MVVM패턴을 의식하며 개발을 하니 처음에는 익숙치 않아 불편하게 느껴졌으나 프로젝트가 진행될수록 패턴 덕분에 체계적인 개발을 할 수 있었다고 생각했습니다.

## 5. 시연영상 링크
https://www.youtube.com/watch?v=cgZLxl4CNIA
