---
title: UI디자인 사이드프로젝트 '믿을 수 있는 동네정보 앱, Villip'
categories: [UIdesign]
tags: [UIdesign]
date: 2023-04-05 13:13:00 +0900
---
# 1. 데스크리서치와 사용자조사
### Bacground
![villip_1.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_1.png)
<br>우리나라 사람들은 다른나라에 비해 통근편의, 환경, 건강, 자녀교육 문제로 이사를 많이 합니다.<br>이에 뒷받침 하는 근거로 국토교통부가 발표한 평균거주기간은 7.5년이며 청년 1인가구는 1.4년이라는 뉴스기사와 연구자료가 있습니다.<br>사람들이 자신이 사는곳에 대해 잘 알지 못해서 이사를 하는게 아닐까? 하는 생각과 이사 간 동네에 대해 알려주는 서비스가 필요하다고 생각했습니다.<br><br>
### 경쟁앱분석
![villip_2.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_2.png)
<br>지역의 상권과 정보를 담고있는 어플리케이션에 대해 사용자 입장에서 조사하고 분석했습니다.<br>사용자들은 네이버지도는 광고가 검색에 우선 노출되는 점, 당근마켓은 거래불이행<br>또는 데이트 목적이나 비속어 사용을 하는 이용자가 많은 점들로 불만을 느끼고 있었습니다.<br><br>
### 문제점과 요구사항
![villip_3.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_3.png)
<br>데스크리서치와 경쟁사 분석을 기반으로 사용자입장에서 보는 문제점과 요구사항 키워드를 도출했습니다.

<br>사용자들은 정확하고 신뢰하고 싶은 동네 정보를 지금보다 손쉽게 얻고 직접 관리하고 싶어했습니다.<br><br>


# 2. 앱 기획
### 해결방안
![villip_4.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_4.png)
<br>사용자들이 말하는 기존 앱들의 문제점과 요구사항을 UI측면에서 해결할 수 있을지에 대한 고민을 했습니다.<br>그리고 해결방안을 토대로 앱의 기획 방향을 정했습니다.<br><br>
### 앱의 목표
![villip_5.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_5.png)
<br>요즘에는 집에만 있어도 다양한 정보를 얻지만 진짜로 믿을만한 정보인지 구별이 어렵습니다.<br>그래서 우리동네 이웃들이 직접 전달해주는 믿을 수 있는 정보의 공간과<br>이사 적응스트레스를 감소시켜 줄 수 있도록 다방면의 동네정보가 담기는 것<br>그리고 이웃들간의 소통과 공유를 통해 콘텐츠가 제작되는걸 목표로 했습니다.<br><br>
### 플로우차트 기획
![villip_8.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_8.png)
<br>플로우 차트를 얕고 넓은 계층으로 만들어서 사용자가 페이지를 빠져 나올때 손쉽게 빠져나올 수 있도록 기획했습니다.<br>그리고 가게상세페이지에서만 채팅을 생성시킬 수 있도록 하여 무분별한 채팅을 줄이는 방향으로 했습니다.<br>활동한 내역이나 스크랩한 정보들은 간편하게 한 페이지(마이페이지)에서 관리 할수 있도록 기획했습니다.<br><br>

# 3. 앱 디자인
### 로고 디자인
![villip_6.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_6.png)
<br>Village(마을)과 lip(입)을 합쳐서 Villip이라는 뜻 입니다.<br>이웃들간의 입을 통해 전해지는 소통으로 연결된다는 의미를 가지고 있습니다.<br>로고의 형태는 로케이션아이콘(loction icon) 2개가 연결된 모양입니다.서로의 위치를 공유한다는 의미를 가지고 있습니다.<br>색상은 적극적이고 활동적인 느낌을 가진 주황색과 이웃의 다양성을 존중한다는 의미에서 보라색을 그라데이션(Gradation)으로 연결시켜서 로고를 완성했습니다.<br><br>
### 디자인 시스템
![villip_7.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_7.png)
<br><br>
### Onboarding
![villip_9.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_9.png)
<br>앱(application)진입 전, 사용자의 상황을 알 수 있는 항목을 체크하여 사용자가 원하는 맞춤정보를 앱에서 볼 수 있습니다.<br>빌립은 단순히 단계는 수를 줄이려 하기보다는 인지적부하와 신체적부하를 줄이는 방향으로 온보딩(Onboarding)을 기획하였습니다.<br>그리고 디자인을 일관성있는 컴포넌트(Componet)로 구성하여 복잡한 설명 없이도 조작을 예측할 수 있게 하였습니다.<br><br>
### 홈화면
![villip_10.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_10.png)
<b>사용자 맞춤 정보 노출</b><br>온보딩을 통해 얻은 결과를 통해 우선순위로 우리동네 장소가 리스트로 표기됩니다.<br>쉼터, 강아지 산책하기 좋은 장소, 택시정류장, 푸드트럭위치 등등 동네 주민만 알 수 있었던 자세한 장소까지도 알 수 있습니다.<br><br>
### 가게 상세 페이지
![villip_11.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_11.png)
<br><b>바쁜시간 알 수 있고 맘에드는 리뷰 고정</b><br>선택한 가게 상세정보에서 손님이 붐비는 시간대를 알 수 있고, 만족한점과 개선한 점의 통계를 한눈에 볼 수 있게 디자인했습니다.<br>그리고 가게 평균메뉴가격과 공지사항으로 가게 방문할때 참고 할 수 있습니다.<br><br>
### 이웃 채팅 페이지
![villip_12.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_12.png)
<br><b>이웃간의 채팅은 용건만 간단히</b><br>가게 상세페이지에서 해당 가게를 이용 중인 이웃에게 가게 내부 상황을 질문할 수 있습니다.<br>웨이팅 여부나 잔여좌석 등의 질문이 가능합니다.<br>질문할때는 텍스트 입력이 아닌 칩(chip)형태로 해서 불편한 대화는 할 수 없도록 했습니다.<br><br>
### 나우 페이지
![villip_13.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_13.png)
<br><b>NOW, 이웃들과 소통하고 고민도 해결</b><br>동네 이웃들과 소통하면서 고민도 취미도 공유할 수 있도록 페이지를 제작했습니다.<br>우리 동네에 관한 뉴스도 한눈에 모아보고,<br>다양한 연령대가 함께 정보를 한 화면에서 공유할 수 있도록 제작했습니다.<br><br>
### 마이 페이지
![villip_14.png](https://raw.githubusercontent.com/pjaehong/pjaehong.github.io/main/assets/img/posts/villip_14.png)
<br><b>스크랩한 동네정보도 손쉽게 관리</b><br>마이페이지에서 동네정보를 손쉽게 관리 할 수 있습니다.<br>그리고 사용자는 동네정보를 추가할 수 있는데 나우에 주제를 추가해달라고 요청하거나<br>우리동네 지도에 장소를 추가요청 할 수도 있습니다.<br><br>
