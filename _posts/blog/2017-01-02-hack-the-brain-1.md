---
date: 2017-01-20 19:09:00 +0900
title: 1. 뇌를 해킹하자.
categories: [Research, EEGBCI]
tags: [research, EEG, BCI, hacking]
---
# 1\. Intro
## 제목을 이렇게 해도 되나..?
해당 글의 카테고리가 "EEG & BCI"인데, 처음 접하는 분야이다보니 카테고리 이름도 맞는지 모르겠다 (추후에 아니다싶으면 바꾸는걸로하고,,)

# 2\. BCI(Brain-Computer Interface)
## BCI란?
최근들어서 뇌파(EEG), BCI(Brain-Computer Interface)에 눈길이 가고 있다. (기반 지식이 다져진다면 brain to brain 도 해보고 싶은 연구하고 싶은 분야이다.)

사실 해당 분야는 영화나 만화에서만 존재할법했는데, 이미 많은 연구가 이루어지고 있는듯 하다. 먼 미래에는 뇌에 칩셋을 이식하거나 헤어밴드 식으로 장비를 가지고 다니면서 생각하는데로 다른 장치를 조정하는 기술이 보편화될것인데(추측), 이 제품이 해킹된다면?...뇌를 해킹하는 엄청난 일을 초래할 수 있다.

해당 연구의 궁극적인 목표는 "뇌를 해킹하자"인데, 아무런 지식이 없는 나로써는 흥미로우면서도 한편으로는 위험한 목표이다. 따지고 보면 뇌를 해킹하는게 아닌 뇌와 연결된 칩셋을 해킹하는거지만, 혹여나 신체에 이상이 가지 않을까? 라는 조심스러운...

## BCI 해킹에 앞선 ToDo들
무튼...보안을 하든 해킹을 하든 해당 시스템의 원리를 파악하는게 먼저이지 않을까 싶다.

그래서 1차적인 목표는 각종 문서를 참고하면서 BCI 장비를 제작해보는 것 이다.
1) EEG(뇌파)를 뽑을 수 있는 장비구축
2) EEG 신호를 받아서 데이터 가공하기
3) 다른 장비로 확장해보기

일단 이정도를 목표로 해서 '뇌 해킹' 세계에 발을 담아본다.

# 3\. 끝으로
해당 분야는 전문가들이 몇 년에 걸쳐서 도출해낸 기술이다. 이 대단한 것을 혼자서 이끌어나갈 수 있을지는 의문이지만c재미있는 분야이기 때문에 충분히 의미있는 일이라고 생각한다.

# 4\. Appendix
아래의 글&링크는 "EEG Hacker([http://eeghacker.blogspot.kr/)"](http://eeghacker.blogspot.kr/)") 블로그에서 따온 내용이다. 이 사람이 처음 시작할때 첨고했던 링크들을 공유해둔...친절한 분 :D

- 원본: [eeg-hacking-begins](http://eeghacker.blogspot.kr/2013/10/eeg-hacking-begins.html)

- Wikipedia:
  > 물론, 모든 사람들은 위키피디아 페이지에서 시작합니다. 괜찮은 페이지예요. 좋은 소개가 되기에는 너무 깁니다. 저는 EEG의 역사에 대한 그것의 토론이 흥미롭다고 생각합니다. 그리고 저는 다른 EEG 주파수 대역에 대한 토론을 좋아합니다. 슬프게도, EEG를 실제로 하는 방법에는 그다지 도움이 되지 않습니다.  
  > - [Electroencephalograph](http://en.wikipedia.org/wiki/Electroencephalography)

- EEG Setup:
  > 매우 기본적인 해커 스타일의 EEG를 어떻게 하는지 간단히 설명할 수 있는 방법은 없습니다. 제가 그걸 고쳐야겠어요. 그 때까지 우리는 다른 사람들의 설명으로 꼼짝도 하지 않아요.  
  > 여기 EEG의 여러 측면에 대해 이야기하는 괜찮은 링크가 있습니다. 하지만 저는 전극, 전극 배치, 그리고 전형적인 EEG 유물의 사진을 좋아합니다. 특히 눈 움직임의 사진을 좋아합니다.  
  > - [The McGill Physiology Virtual Lab](http://www.medicine.mcgill.ca/physio/vlab/biomed_signals/eeg_n.htm)

  > BCI2000 사람들은 또한 많은 좋은 정보를 가지고 있다. 다음은 전극, 배치 및 일반적인 신호 아티팩트에 대한 기본 사항입니다.  
  > - [User\_Tutorial:EEG\_Measurement\_Setup](http://www.bci2000.org/wiki/index.php/User%5C_Tutorial:EEG%5C_Measurement%5C_Setup)

- Typical EEG Signals:
  > 위의 링크는 특히 EEG 시스템에 의해 수집되는 바람직하지 않은 신호인 artifacts의 대표적인 신호에 대해 언급하였다. 이러한 공예품들은 보통 뇌 활동과 관련이 없으며, 이것이 그들이 나쁘다고 여겨지는 이유이다.  

  > EEG의 실제 뇌 신호는 종종 주파수 내용에 기초하여 논의되고 분석됩니다. 이것들은 소위 알파파, 베타파, 테타파 등입니다. 위의 위키피디아 페이지는 이러한 다른 주파수 대역에 대해 설명합니다. 아래 링크도 마찬가지입니다. 

  > EEG 신호를 논하는 또 다른 방법은 파장의 모양에 의한 것이지 주파수 내용물에 의한 것이 아니다. 이것은 파도의 형태학이다. EEG 신호의 일부 형태학적 특징:  
  > - [Normal EEG Waveforms](http://emedicine.medscape.com/article/1139332-overview#aw2aab6b3)

- Finally,
  > 다음은 EEG에서 볼 수 있는 몇 가지 일반적인 유형의 신호에 대한 보다 공식적인(구체적이고 상세한!) 토론입니다. 알파파에 대해 논의하는 데 많은 시간을 할애합니다.  
  > - [Niedermeyer_1999.pdf](http://www.ccs.fau.edu/~bressler/EDU/NSP/References/Niedermeyer%5C_1999.pdf)