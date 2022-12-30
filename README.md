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
* :white_check_mark: 소셜 로그인
* :white_check_mark: 부동산 정보 및 서비스
* :white_check_mark: kakao Map 활용 

## 3. 설계
* 아키텍처 <p>
  ![image](https://user-images.githubusercontent.com/75747197/210081322-cfc57a10-586e-42d7-9b46-ad7db43ca24a.png)
* Usecase Diagram <p>
![image](https://user-images.githubusercontent.com/75747197/210095983-60c9e00d-17a4-497a-a5c7-0be8e83863ec.png)

* Rest API <p>
  |Method|URL|설명 |
  |----|----|----|
  |GET|/rest/house/interest||
  |GET|/rest/house/search/housedeal/{aptCode}||
  |POST|/rest/house/interest||
  |POST|/rest/house/search/dongList||
  |DELETE|/rest/house/interest/{aptCode}||
  |GET|/rest/area||
  |GET|/rest/area/{sidoName}||
  |GET|/rest/area/{sidoName/{gugunName}}||
  |GET|/rest/notice/article/{no}||
  |DELETE|/rest/notice/delete/{no}||
  |GET|/rest/notice/list||
  |PUT|/rest/notice/modify||
  |GET|/rest/notice/search/{title}||
  |POST|/rest/notice/write||
  |GET|/rest/qna/answer/{questionno}||
  |DELETE|/rest/qna/answer/delete/{answerno}||
  |PUT|/rest/qna/answer/modify||
  |POST|/rest/qna/answer/write||
  |GET|/rest/qna/question||
  |GET|/rest/qna/question/{no}||
  |PUT|/rest/qna/question/complete/{questionno}||
  |DELETE|/rest/qna/question/delete/{questionno}||
  |PUT|/rest/qna/question/modify||
  |POST|/rest/qna/question/write||
  |DELETE|/rest/user/delete/{memberid}||
  |POST|/rest/user/findpwd||
  |GET|/rest/user/info/{memberid}||
  |POST|/rest/user/join||
  |POST|/rest/user/kakao||
  |POST|/rest/user/login||
  |GET|/rest/user/logout/{memberid}||
  |PUT|/rest/user/modify||
  |POST|/rest/user/refresh||
  |PUT|/rest/user/updatepwd||
  

## 4. 리뷰
* 프로젝트 설계에 맞게 다양한 기능을 구현하고 기능들을 유기적으로 연결하는 과정에서 명확한 설계의 중요성을 알 수 있었습니다.
* SSAFY 교육과정에서 배운 내용을 실제로 개발에 사용함으로서 알고있는 지식에 대한 이해도를 높일 수 있었습니다.
* 특히 Java Spring의 MVC패턴과 Vue의 MVVM패턴을 의식하며 개발을 하니 처음에는 익숙치 않아 불편하게 느껴졌으나 프로젝트가 진행될수록 패턴 덕분에 체계적인 개발을 할 수 있었다고 생각했습니다.

## 5. 시연영상 링크
https://www.youtube.com/watch?v=cgZLxl4CNIA
