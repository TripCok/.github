# 📍 Tripcok 트립콕 📍
# 📌 Tripcok 트립콕 📌
# ![TripCok Preview](images/Tripcok_readme.png)

---

## **📌 프로젝트 목표**

### 사용자 로그 데이터를 활용한 여행 추천 서비스
- 사용자의 관심사, 과거 참여 기록 기반으로 여행지 추천을 진행하여 사용자 맞춤 여행지 추천 기능 제공

### 모임 생성 및 여행 동반자 생성 서비스
- 사용자는 자신의 관심자와 관련된 모임에 가입 & 공통된 관심사를 공유하는 사람들과의 모임 구성 가능

### 관리자 페이지 
- 관리자 페이지에서는 모델의 정확도 및 일별/월별 데이터 집계 정보를 모니터링할 수 있는 기능을 제공

## 📚 기술스택
Language&build tool
<br>
<img src="https://img.shields.io/badge/Java-536DFE?style=flat-square&logo=Java&logoColor=white"/> <img src="https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=Gradle&logoColor=white"/>
<br>
Framework
<br>
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat-square&logo=Spring Boot&logoColor=white"/>
<br>
Library
<br>
<img src="https://img.shields.io/badge/Swagger-85EA2D?style=flat-square&logo=Swagger&logoColor=white"/>
<br>
Database
<br>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=Redis&logoColor=white"/>
<br>
Deploy
<br>
<img src="https://img.shields.io/badge/Amazon S3-569A31?style=flat-square&logo=Amazon S3&logoColor=white"/>



## 🔧 사용 툴
<img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/> <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=Git&logoColor=white"/>
<img src="https://img.shields.io/badge/IntelliJ IDEA-000000?style=flat-square&logo=IntelliJ IDEA&logoColor=white"/>
<img src="https://img.shields.io/badge/Sourcetree-0052CC?style=flat-square&logo=Sourcetree&logoColor=white"/>
<img src="https://img.shields.io/badge/Notion-000000?style=flat-square&logo=Notion&logoColor=white"/>
<img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=Postman&logoColor=white"/>
<img src="https://img.shields.io/badge/Slack-4A154B?style=flat-square&logo=Slack&logoColor=white"/>
<img src="https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=Figma&logoColor=white"/>

## **⏳ 프로젝트 기간**
**2024년 11월 14일 ~ 2024년 12월 31일**

## **🪧 작업 간략 소개**

### Spring Server -> [link](https://github.com/TripCok/TripCok_server)
TripCokServer는 여행지, 모임, 게시글, 댓글 등 여행 플랫폼에서 필요한 핵심 기능을 제공하는 Spring Boot 기반의 서버

**구성**

- 회원 관리, 모임 생성 및 관리, 여행지 정보 조회, 게시글 및 댓글 작성 기능 제공

---

### Thymeleaf Admin -> [link](https://github.com/TripCok/TripCok_server/tree/0.2-dev/src/main/resources/templates)
Thymeleaf로 구현된 페이지는 관리자 전용(Admin) 페이지로, 매니저들이 서버의 다양한 데이터를 효율적으로 관리하고 분석할 수 있도록 설계

**구성**

사용자 증감률, 여행지의 시간대별 조회수, 모임 신청의 증가 및 감소 추이와 같은 주요 지표를 시각적으로 확인 가능 이러한 데이터는 차트, 그래프 등의 시각화 자료로 제공되어 데이터의 흐름과 변화를 직관적으로 파악 가능

- 여행지 데이터: 여행지의 상세 정보 수정, 삭제, 추가 등 여행지 관리 기능
- 사용자 데이터: 사용자 프로필, 활동 기록, 상태 변경 등 사용자 정보 관리 기능
- 모임 데이터: 모임의 생성, 수정, 삭제 및 상태 관리 기능
  
---
  
### React native App -> [link](https://github.com/TripCok/TripCok_App)
TripCok React Native 앱은 사용자 중심으로 설계된 여행 및 모임 플랫폼으로, 개인의 취향에 맞춘 여행지와 그룹 추천 서비스를 제공

**구성**
 
- 맞춤형 추천: 사용자 선호도와 활동 데이터를 기반으로 개인화된 여행지와 모임 추천
- 모임 활동: 모임 생성, 참여, 관리 등을 통해 네트워킹 강화와 커뮤니티 활성화
- 실시간 데이터 제공: 최신 정보와 동기화된 데이터를 통해 항상 업데이트된 상태 유지
- 편리한 UI/UX: 직관적이고 간편한 탐색 및 관리 인터페이스로 사용자 편의성 제공

---
  
### Model -> [link](https://github.com/TripCok/TripCok_models)
TripCok 의 추천 시스템을 담당하는 부분으로, 입력받은 데이터로부터 추천 여행지를 반환

** 구성 **

- 공용 API 이용: `한국관광공사_국문 관광정보서비스 API`로부터 관광지 데이터를 내려받아 이를 전처리하여 사용
- 텍스트 기반 임베딩: 한국어 특화 자연어 처리 모델 `ko-sroberta-multitask`로 개별 여행지의 "개요" 텍스트 전처리 후 이를 기반으로 한 추천 시스템 구축
- 모듈 인터페이스: 추천 시스템의 I/O 및 타 모듈과의 인터페이스/API 시스템 구현


### Infra
- Kafka
- Spark
- Airflow
- Superset
- DB(MariaDB, Postgres)
- Zenkins
- Flask




## **👥 Tripcok Contributors (RIP...)**

```plaintext
==================+=========================-----=------============*%%%%%###***++==-
================================================================+#%%%####%###*+++=-:.
=============================================================*#%%%#######%*#**++=-:..
---------------------------------=====-=-================+*%%%%###########+#**++==--:
--------------------------------------------------==++*%%%%%##############****++++===
-----------------------------------------------------=%###############***#****+++++++
-----------------:------------------------------------%*#######**--******#******+++++
---::::::::::::::::::::::::::::::::::::---------------%*##*****+++++*****#*+*++++++++
:::::::::::::::::::::::::::::::::::::::::::::::::::::-%********++++++*++***++++++***#
::::::::::::::::::::::::::::::::::::::::::::::::::::::#+*******++++***+++***##%%#*===
::::::::::::::::::::::::::::::::::::::::::::::::::::::#+******++**###%%#+*#=---------
::::::::::::::::::::::::::::::::::::::::::::::::::::::#++*###%**+=--::::-+#----------
::::::::::::::::::::::::::::::::::::::::::::::::::::::##*==---+*%@#-:::::+%----------
::---::::..::--:...::::::::::....::::::::::::::::%@@@##*==---*@*#@@%:----+%-==-==----
::==-:---:..---:...::::...........:::+@@@*::::::*@##@@%*==---=**===+-----+%=====----=
:::::::::...::::::-%#*#+....::::::::=@@*=@=:::::-*+==+#*==-===++====----=+%======---=
-:---:::::..::-::-#++==*:.:-%##%=:::*%+=+%+:::::::*++-**+======**+=*+--==+#======--==
-:---:---:..:::::-#+++==::-%%=++%-::*@#*%@=:::=*@@**++@@#+==+*====-:#**+=+#+=======-=
-:::::---:.....::+=+***:.:*@%+++@%:::...:+=:=@@@@@%=*@@@@@@##*......**#**+#+========-
=+=----:.....:---::--=-:-+@@@#+*@+:::.....--+@@@@@@@@@@@@@@%#-......*#*#*#*++========
=-=--:::....-===---:..:--=#@#=::#=:-----:.-=%@@@@@@@@@@@@@@@#-:.....+******####****##
--=:......:-==+=-------===*@*...*=:=-++++*##@@@*........:%@@%=:.....+***#*******++*++
:::.......:==+*===--===++==#+...:-++++-::-+*#@*=........:%@@%=.:....+##*#**++++++++==
::::::::::===++===-=--=**+-:-....:#*:...::=###%=........:+%%#=.:....-*#*#**++++++++==
----------+*===-=-----===--:..:..-#%%%###%%####%*+-:....:#*##-.:....:##*#*%**++++++==
-----------=+*+=--=-----=--::::.::*%%%%%%%%%##%@@@@@@@@@@@@%*-:::....+#*#*%**++++++==
--------------+=---==-===:-:::::::#%%%%%%%**+*#@@@@@@@@@@@@%*-:::....+****#*+++=+++++
--------------+****#%@@%=-::::::::#%%%%@%%*#+*#@@@@@@@@@@@@%*-:::....=**+*##+++++=+++
--------------+@@%%%%*+=---::::.:=#%%%%@%%%%++#@@@@@@@@@@@%**==+=--::-=-**##+++++++++
----------------:::::::::::=++*+++#%%%%@%%%#++*@@@@@@@@@@@%**+=-=+*=--:-**##+++++++++
------------::::-:::::-::::-++*+++*%%%%@%%%*=+*#@@@@*@@@@@****---=+=-::+%###+++++++++
----------=-::::-:::-----:::=+#*++*@%%%#%%%===+*@@@@%@@@@%+***---=+==--+**#%##**+++++
------=====-:----------------+**+++++..:=%%%%%%*@@@%*#@@@%#***=--=+++--+++##+++*###*+
-=+*#%%%%%%---------=+++=========++**%@%..#%@@**@@@@**@@@%***+*=-=+++--+++##++++++++*
```

## TEAM 4

| 사용자 이미지 | 사용자 이미지 |
|----------------|----------------|
| <img src="https://github.com/user-attachments/assets/1d9954e4-f162-4ff5-8acf-b749fb1d5cd0" width="50%" style="display:block; margin:auto;"> | <img src="https://github.com/user-attachments/assets/faebaeaf-1722-4a10-a398-1fba10ecc2a3" width="50%" style="display:block; margin:auto;"> |
| **[PM] 이정훈** | **[TL] 김령래** |
| <img src="https://github.com/user-attachments/assets/1317f516-941b-4258-9f44-b23f40546cea" width="50%" style="display:block; margin:auto;"> | <img src="https://github.com/user-attachments/assets/18292e29-8bab-4c65-abd0-fadf6e253d02" width="50%" style="display:block; margin:auto;"> |
| **[AC] 최하람** | **[AA] 정세현** |
| <img src="https://github.com/user-attachments/assets/6c572c13-2f18-4c4b-bd04-91cadbc727cd" width="50%" style="display:block; margin:auto;"> |  |
| **[GL] 김예지** | |

