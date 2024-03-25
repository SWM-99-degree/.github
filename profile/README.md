

# "자리:Bean" - 카페 위치 탐색 및 예약 서비스 
![](https://hackmd.io/_uploads/HykQw6Nsh.png)
    
카페 매장과 손님을 연결해주는 매칭 서비스로 손님들은 원하는 카페를 쉽게 찾을 수 있고, 카페는 예약과 주문을 받아 더욱 효율적인 운영이 가능해진다.

## Android
![image](https://github.com/SWM-99-degree/.github/assets/57629885/40ea1556-34ec-4289-a1e4-997395a400e8)
[다운로드](https://play.google.com/store/apps/details?id=com.jari_bean.app)


## iOS
![image](https://github.com/SWM-99-degree/.github/assets/57629885/17fbfbb4-ed5d-4c51-b0fe-b6cabffc00bb)
[다운로드](https://apps.apple.com/kr/app/%EC%9E%90%EB%A6%AC-bean/id6471389388?l=ko-KR)
<br>
<div align=left>

## 프로젝트 개요
### 소프트웨어 마에스트로 14기 - 팀 99℃
- **자리:Bean - 카페 예약 및 매칭 서비스**
- 개발 기간 : 2023.6.20 ~ 2023.11.23
- 🗄 [ 기획서](https://lineno2.notion.site/d4f2664412df48b6b9412e57b21bf90a?pvs=4)
- 👩‍💻 [ 소개 노션 페이지](https://lineno2.notion.site/99-e3ec59eb3ab64b56a647f53837307cac?pvs=4)

### 카페의 자리를 잡기 위해 시간을 낭비하고 계신가요?
- 🔥 걸어서 10분 거리 카페와의 **매칭**을 통해 카페를 찾을 수 있어요
- 📒 **예약**을 통해 카페의 자리를 확보할 수 있어요
    


## 사용된 기술 스택 및 아키텍처
### AWS 아키텍처
![image](https://github.com/SWM-99-degree/.github/assets/57629885/a4e2d6cd-7963-46bd-a35c-8b24943a6533)

### 시스템 구성도
![image](https://github.com/SWM-99-degree/.github/assets/84831081/0d050e8a-d558-4805-b417-8e914260e3fc)

    

### 활용한 스택
#### 🪃 Backend
- Spring Boot
- FastAPI
- Node.js
- Redis
- MongoDB
- ElasticSearch
- Komoran
- JPA
- Docker
- Github actions
    
#### 🏈 Frontend
[앱]
- Flutter
- Riverpod
- Sqlite
- FCM
- Dio
- Oauth
- Fastlane

[웹]
- Svelte
- FCM

#### 🌐 Infra
[AWS]
- EC2
- ELB
- SQS
- Elasticache
- API gateway
- S3
- CloudFront
- Lambda

#### 👥 협업 툴
- Discord
- Github issue
- Notion



## 프로젝트 기능 소개
| 로그인 |
| - |
|  ![](https://hackmd.io/_uploads/HJjUjp4i2.png)|
| - **KAKAO**, **GOOGLE**, **APPLE** 의 OAuath2 기능을 이용하여 로그인 기능을 구현하였습니다. |

 | 매칭 기능 |
 | - |
 |![matching](https://hackmd.io/_uploads/BJsA5TEsh.png)|
 | - 주변에 있는 카페에 **매칭요청**을 보내요! <br> - 원하는 인원을 기입해서 매칭 요청을 보낼 수 있어요! <br> - **`RedisSet`** 과 **`FCM`** 을 통해서 매칭을 수락하고 거절할 수 있어요!   <br> - **`FCM`** 를 활용해서 카페에 오는 매칭을 어떠한 조작 없이 실시간으로 받을 수 있어요! <br> - **`RedisQueue`** 를 지속적으로 오고가는 통신을 일정한 기간을 두고 가져올 수 있어요! <br> - 카카오맵 API를 가져와 길찾기 기능을 얻을 수 있어요!|
 
 | 예약 기능 |
 | - |
 | ![image](https://github.com/SWM-99-degree/.github/assets/84831081/908a71f1-6659-4cf7-9a2f-97269bd02556) |
 | - 원하는 위치, 원하는 조건, 원하는 시간에 **`좌석 예약`** 을 해 보세요! <br> - **`elasticsearch`** 를 활용하여 검색 속도를 높였어요! <br> **`MongoDB`** 를 통해서 원하는 조건에 따라 카페를 조회할 수 있어요! <br> - **`특별한 알고리즘`** 을 통해서 앞뒤로 30분 예약이 되어 있더라도 예약 창을 볼 수 있어요! |
 

| 점주 웹 사이트 |
| - |
| ![image](https://github.com/SWM-99-degree/.github/assets/84831081/edc6c7a4-eced-4621-9c40-f77879cdc2a4) |
| - 점주 웹페이지에 가입할 수 있어요! 이 웹은 자체 로그인만 가능해요. <br> - **`svelte`** 를 활용하여 만들었어요! <br> - 점주 웹을 통해서 당일 예약된 상황을 볼 수 있어요! <br> - 점주 웹을 통해서 매칭을 거절하거나 수락할 수 있어요! <br> - 수락 또는 완료를 누를 수 있어요! |


<br>

## 기술적 고민
- 🕐 [**`Redis Pub/Sub`**, 어떻게 쓰는거죠?](https://psy-choi.tistory.com/40)
- 🎨 [**`Elasticsearch`** 와  **`mongoSearch`** 중 어떤 것이 성능적으로 빠를까?](https://psy-choi.tistory.com/33)
- ⚙️ [**`SSE`** 와 **`FCM`** , 무엇을 실시간 통신을 위해 사용해야 할까?](https://psy-choi.tistory.com/47)
- 🌀 [**`SQS`** 를 통한 전송보장, 어떻게 할까요?](https://psy-choi.tistory.com/44)
- 🎫 [**`Issue`** 관리와 **`Commit Message`** 를 어떻게 쓸까?](https://psy-choi.tistory.com/45)
- ✍️ [**`CICD`** 구축을 위한 우당탕탕 **`Github actions`** 일기](https://psy-choi.tistory.com/28)

<br>

## ERD
![SWM-jariBean (2)](https://github.com/SWM-99-degree/jariBean/assets/85926257/5dd25374-7443-4c90-8997-a04bf7fa27c5)
<br>

<hr>



### 팀원 소개
|최기성|김상현|이호선|
|:---:|:---:|:---:|
|![%EC%B5%9C%EA%B8%B0%EC%84%B1%20%ED%94%84%EB%A1%9C%ED%95%84](https://github.com/SWM-99-degree/.github/assets/84831081/de57e7ef-c40a-4041-8063-a99d50b82e2a?width=50)|![Untitled](https://github.com/SWM-99-degree/.github/assets/84831081/35c44282-1dbb-4cec-b843-c0686b6db237)| ![Your Name](https://github.com/SWM-99-degree/.github/assets/84831081/6a060570-3ee8-4d14-87b6-d0ba90bbc5eb)|
|[@psy-choi](https://github.com/psy-choi)|[@isayaksh](https://github.com/isayaksh)|[@LineNo2](https://github.com/LineNo2)|[@high2092](https://github.com/high2092)|
