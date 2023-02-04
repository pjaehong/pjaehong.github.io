---
date: 2018-04-08 19:09:00 +0900
title: 3. EEG 칩셋(TGAM1) 분석
categories: [Research, EEGBCI]
tags: [research, EEG, BCI, hacking]
---
# 1. 분석은 RAW하게
나는 보통 프로젝트를 진행하면 대상이 뭐든간에 raw하게 접근하고 관련된 것들을 찾아본다. raw하게 보는건 사서 삽질을 하는건데, 이러면서 배우는게 생각보다 많고 은근히 재미있다!! 사서 삽질한 내역들을 대충 보면 이러하다.
 - GPU keylogger프로젝트할때 커널 소스 분석 및 커널 구조 공부
 - 응용프로그램 or 각종 서비스의 작동 원리가 궁금해서 진행한 바이너리 리버싱
 - 등등..

이번 프로젝트에서도 raw단부터 분석을 할거고 대상은 장비 내부의 EEG칩셋(TGAM1) 정도만 볼거다. 그리고 해당 장비의 메인 칩셋을 분석하는 이유는 간단하다.
 - EEG 측정 장비를 만들어보고 싶었고
 - 해당 장비와 아두이노(또는 기타 kit)를 연결할 일이 있을듯 해서!

하지만 이런 이유를 떠나서, 장비를 열어보고 나니 별게 없다는걸 깨닳았다. 단지 느낀점은 "아 이렇게 생겨먹었구나" 정도..?

이 게시글에서 여기까지만 읽어도 많이 읽은거다. 솔직히 밑에는 더 읽을것도 없고 얻어갈 정보도 없으니, 할 일이 많은 분들은 여기까지만 읽고 돌아가도 좋을 법하다! (적극추천)

# 2. 장비 오픈
![neurosky](/posts/neuronow3.jpeg)

[이전 포스트](https://blackcon.github.io/posts/hack-the-brain-2/)에서도 외형 사진을 올려서 알겠지만, 제품을 배송받자마자 바로 나사들을 풀었다! 

내부구조는 생각보다 심플한 구조다. 내부에는 board 2개가 겹쳐져있고, 뇌파측정을 위한 파란색 연장선이 외부로 뻗어 있다.

**1) 메인보드** 
- 이미지에 있는 2개의 녹색 기판 중, 뒷쪽에 있는 큰 기판
- 메인보드까지 꺼내보지 않았지만, 전원, 블루투스, TGAM1모듈을 연결하는 기능으로 추측됨

**2) TGAM1**
- NeuroSky에서 제작한 EEG(뇌파)를 측정하는 메인 칩셋
- ThinkGear [ASIC](http://terms.naver.com/entry.nhn?docId=933064&cid=43667&categoryId=43667) Module의 준말
- 참고 : [TGAM1 Spec Sheet](http://wearcam.org/ece516/neurosky_eeg_brainwave_chip_and_board_tgam1.pdf) 

**3) 파란색 연장선**
- EEG Electrode "EEG" : 뇌파측정 단자
- Reference electrode "REF" : 기준전극을 잡기위한 단자

# 3. 앞서 말했듯이
본 글의 서론에서도 말했듯이 이 글에서 얻은 정보는 없을것이다. 이런 글의 마무리도 어떻게 해야될지 모르겠고, 그냥 여기서 급 마무리를 짓는다. :D