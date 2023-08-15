<div align=center>

# "jari:Bean" - 카페 위치 탐색 및 예약 서비스 
![](https://hackmd.io/_uploads/HykQw6Nsh.png)
    
카페 매장과 손님을 연결해주는 매칭 서비스로 손님들은 원하는 카페를 쉽게 찾을 수 있고, 카페는 예약과 주문을 받아 더욱 효율적인 운영이 가능해진다.

### 🙆‍♂️[~~배포 페이지~~]🙆‍
<br>
<div align=left>

## 프로젝트 개요
### 소프트웨어 마에스트로 14기 - 팀 99℃ 의 프로젝트
- **jari:Bean - 카페 예약 및 매칭 서비스**
- 개발 기간 : 2023.6.20 ~ 진행중
- 🗄 [ 기획서](https://lineno2.notion.site/d4f2664412df48b6b9412e57b21bf90a?pvs=4)
- 🎥 [ 피그마 페이지](https://www.figma.com/file/kprQo5meL68mthIIBAN0yq/%EC%B9%B4%ED%8E%98-%EB%B9%88-wireframe?type=design&node-id=0-1&mode=design)
- 👩‍💻 [ 소개 노션 페이지](https://lineno2.notion.site/99-e3ec59eb3ab64b56a647f53837307cac?pvs=4)

### 카페의 자리를 잡기 위해 시간을 낭비하고 계신가요?
- 🔥 걸어서 10분 거리 카페와의 **매칭**을 통해 카페를 찾을 수 있어요
- 📒 **예약**을 통해 카페의 자리를 확보할 수 있어요
    

<br>

### 팀원 소개
|최기성|김상현|이호선|
|:---:|:---:|:---:|
|![최기성 프로필.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/795d807d-7afe-41ba-91ae-b92bf3561154/%EC%B5%9C%EA%B8%B0%EC%84%B1_%ED%94%84%EB%A1%9C%ED%95%84.png)|![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/08ec94d7-0b18-4ba5-b70e-7984ed16a58b/Untitled.png)|![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0a100e12-be8c-48ec-822c-06eaf36a53d5/Untitled.png)|
|[@psy-choi](https://github.com/psy-choi)|[@isayaksh](https://github.com/isayaksh)|[@LineNo2](https://github.com/LineNo2)|[@high2092](https://github.com/high2092)|
    
<br/>

## 사용된 기술 스택 및 아키텍처
### AWS 아키텍처
![image](https://github.com/SWM-99-degree/.github/assets/84831081/3b9c613d-111b-4c0c-8255-969087cc6cd4)



### Backend 아키텍처
![image](https://github.com/SWM-99-degree/.github/assets/84831081/509015e7-3476-45bc-ae8a-79f79798633e)
    

### 활용한 기술
#### 🪃 Backend
- Spring Boot
- EC2, ELB, SQS, Elasticache, API gateway, Open Search
- Redis
- MongoDB
- ElasticSearch
- Komoran
- JPA
- Github actions
    
#### 🏈 Frontend


## 프로젝트 기능 소개
| 로그인 |
| - |
|  ![](https://hackmd.io/_uploads/HJjUjp4i2.png)|
| - **KAKAO**, **GOOGLE**, **APPLE** 의 OAuath2 기능을 이용하여 로그인 기능을 구현하였습니다. |

| LOG - 친구와의 상호작용 |
| - |
| ![LOG_new__](https://user-images.githubusercontent.com/73420533/207790704-b70dcc83-1a47-4433-99ff-2545c472b601.gif)  |
| - 다른 사용자와 **친구**가 되어 서로의 일상을 공유해 보세요! <br> - 친구의 로그를 조회하고 **이모티콘**을 남길 수 있어요! |

 | 매칭 기능 |
 | - |
 |![matching](https://hackmd.io/_uploads/BJsA5TEsh.png)|
 | - 주변에 있는 카페에 **매칭요청**을 보내요! <br> - 원하는 인원을 기입해서 매칭 요청을 보낼 수 있어요! <br> - **`RedisSet`** 과 **`FCM`** 을 통해서 매칭을 수락하고 거절할 수 있어요!   <br> - **`SSE`** 를 활용해서 카페에 오는 매칭을 어떠한 조작 없이 실시간으로 받을 수 있어요! <br> - **`RedisQueue`** 를 지속적으로 오고가는 통신을 일정한 기간을 두고 가져올 수 있어요! <br> - 카카오맵 API를 가져와 길찾기 기능을 얻을 수 있어요!|
 
 | GOAL - 라벨을 통해 관리되는 목표 |
 | - |
 | ![GOAL__](https://user-images.githubusercontent.com/73420533/207793713-5cdf10d3-c8fd-42fd-a3b7-9580c0fb9d27.gif) |
 | - 데일리 목표를 설정하고 **일정에 등록한 라벨을 통해 목표를 달성**해 보세요! <br> - 일정이 완료되면 설정된 라벨을 통해 목표 달성률이 자동으로 채워져요 <br> - 달성률을 달력에서 확인할 수 있어요 |
 
 | MAP - 지도로 보는 데일리 플랜 |
 | - |
 | ![MAP__](https://user-images.githubusercontent.com/73420533/207800199-6724abf2-f429-400f-a27a-3aca57abc7b6.gif) |
 | - **일정에 설정된 위치**를 통해 하루 동안의 동선을 확인할 수 있어요 <br> - **친구의 동선을 함께** 조회할 수 있어요 <br> - 모든 일정을 한 눈에 파악할 수 있는 전체 보기, 일정을 클릭하면 해당 위치로 이동하는 LOG 리스트를 이용할 수 있어요 |
 
| LOG - 일정 생성 |
| - |
| ![LOG생성__](https://user-images.githubusercontent.com/73420533/207800969-d3ab5cff-d724-4098-b12e-37cd803df171.gif) |
| - 제목, 태그, 시간, 중요도, 공개 여부, 위치, 라벨, 메모 정보를 입력하고 새로운 일정을 생성해 보세요! <br> - 태그 / 라벨을 생성, 삭제, 변경하고 설정할 수 있어요 <br> -일정에 등록한 라벨은 목표에 자동으로 연동돼요 <br> - 장소 검색 API를 이용하여 위치를 검색하고 설정하면 지도 탭에서 위치를 확인할 수 있어요 |

| MAIN - 회원가입 로그인 |
| - |
| 사진 |
| - 카카오/ 깃허브 / 기본 회원가입 후 서비스를 이용해요 <br> - 프로필 사진과 정보의 입력이 잘못된 경우 메세지가 표시돼요 |

| FRIEND - 친구와 함께쓰는 데일리 플래너 |
| - |
| 사진 |
| - ID로 친구를 검색하고 친구 신청을 할 수 있어요 <br> - 햄버거 바에서 친구 요청을 관리하고 나에게 온 알림을 확인해요 <br> - 친구가 되면 친구의 데일리 플래너의 모든 항목을 구경하고, 이모티콘, 실시간 그림일기로 소통할 수 있어요 |


<br>

## 기술적 고민 - [노션](https://mikaniz.notion.site/127548b26c254f42bf85f8963f8fd2be?v=60b5863159d845cbb77a1c38fa231952) / [기술 발표](https://www.youtube.com/watch?v=A--cReu9rgE)
- 🕐 [**`SSE`** 과 **`FCM`** 중 어떤 것을 택해야 할까?](https://mikaniz.notion.site/1bf8fe670232484d84dbd880f176b438)
- 🎨 [**`Elasticsearch`** 와  **`mongoSearch`** 중 어떤 것이 성능적으로 빠를까?](https://mikaniz.notion.site/Redis-socket-io-f2701f4bb4354e93ab3f8b8656801cc6)
- 🔏 [로그인 중 토큰을 탈취 당하지 않으려면 어떻게 해야 할까?](https://mikaniz.notion.site/af770bf344f949bbaa9b3eda6cc2006c)
- 🚶 [**`MongoDB`** 와 **`PostSQL`** 중 어떤 DB를 활용하는 것이 좋을까? ](https://mikaniz.notion.site/Raw-Query-c66a2b0b0e6f4db692d78db72cc308f5)
- ⚙️ [완벽한 **`RESTful API`** 를 쓸 수 있을까?](https://mikaniz.notion.site/RESTful-API-2aa885e4362e41d786492515d6e0f834)
- ✍️ [MSA를 굳이 활용할 필요가 있었을까? **`fastAPI`** 를 쓴 이유!](https://mikaniz.notion.site/LOG-550b280e89fc46f184f4d44e7691837d)
- 🌀 [**`애니메이션`** 을 통한 한층 더 기분 좋은, 고퀄리티의 UI/UX](https://mikaniz.notion.site/UI-UX-70c561f8f0ba45d6adaaa5da9b160ea7)
- 🎫 [**`Issue`** 관리와 **`Commit Message`** 를 어떻게 쓸까?](https://mikaniz.notion.site/PR-95732bea02ab4b3fa3f5459d347af5a1)
- ✍️ [**`CICD`** 구축을 위한 우당탕탕 **`Github actions`** 일기](https://mikaniz.notion.site/PR-95732bea02ab4b3fa3f5459d347af5a1) 

<br>

## ERD
<img width="810" alt="image" src="https://user-images.githubusercontent.com/73420533/207799380-63d3de7a-1c3f-4757-a878-0f9d400765ea.png">
<br>

<hr>

## 개발 환경에서의 실행 방법
```sh
$ cd ./client
$ npm ci
$ npm run build
$ cd ../server
$ npm ci
$ npm start
```
