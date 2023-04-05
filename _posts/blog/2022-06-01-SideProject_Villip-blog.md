---
title: [UI디자인]사이드프로젝트 '믿을 수 있는 동네정보 앱, Villip'
categories: [UIdesign]
tags: [UIdesign]
date: 2023-04-05 13:13:00 +0900
---
# 1. 
- list와 dict 의 사용법 

# 2. 수업내용
## 2.1) 조건문이란?
- 프로그래밍 흐름 상 특정한 조건에서만 실행해야하는 코드가 있기 마련인데, 이 때 크드를 분기(branch)하기 위해서 사용되는 문법이다.
- 조건문은 중첩 

## 2.2) 조건문 문법
- 전체적인 문법 구조
  - if, elif, else 의 순으로 사용되며
    - if문의 조건문에서 False가 발생할 경우 elif로 넘어간다.
    - elif 의 조건문이 False가 발생하면 그 다음의 조건문(elif 또는 else)을 검증한다.
    - if와 elif 가 모두 충족되지 않으면(False) else 분기가 처리된다.
  - 주의: if, elif, else의 끝에는 `콜론(:)`을 반드시 입력하여야 한다.
  - 하나의 분기문 코드는 `들여쓰기를 기준`으로 구분한다.
  - 문법
    ```python
    if 조건문1: #True 또는 False인 결과에 따라서 조건을 수행함
        코드 분기 (1)
    elif b == a: #조건문2:
        코드 분기 (2)
    elif b < a: # 조건문3:
        코드 분기 (3)
    else:
        코드 분기 (4)
    ```
  - 예제
    ```python
    a = 10
    b = 5
    if b > a: #조건문1: True 또는 False인 결과에 따라서 조건을 수행함
        print( " B > A")
    elif b == a: #조건문2:
        print( " B == A")
    elif b < a: # 조건문3:
        print( " B < A")
    else:
        print( "this is  else " )

    print( "done" )
    ```
- `주의`
  - `if, elif, else`의 구조가 아닌 `if, if, if`의 구조일 경우
  - 첫번째 조건문이 True로 성립하더라도, 이 후의 조건문도 모드 체크한다.
  - 예시
    ```python
    a = 5
    b = 5

    if b >= a: #조건문1: True 또는 False인 결과에 따라서 조건을 수행함
        print( " B >= A")
        print( " B >= A")
        print( " B >= A")
        print( " B >= A")
        print( " B >= A")
    if b == a: #조건문2:
        print( " B == A")
    if b < a: # 조건문3:
        print( " B < A")

    print( "done" )
    ```
## 2.3) 중첩 조건문
- 조건문 안에 또 조건문이 있는 구조이다.
- 예시
    ```python
    a = 400
    b = 400
    if a > b :   # 중첩 조건문
        if a == b:
            print( "a == b" )
        else:
            print( "kkk" )
    elif a < b:
        if b > 1000:
            print( "b > 1000" )
        elif b == 1000:
            print( "b == 1000" )
        else:
            print( "b < 1000" )
    else:
        print( "a is {0}".format( a ) )
    print( 'done' )
    ```

# 3. 백준 알고리즘 (조건문 문제 풀기)
- link: [두 수 비교하기](https://www.acmicpc.net/problem/1330)
- 코드 예제
    ```python
    a = input("숫자:" )
    var = a.split(" ")# "100 20" -> ["100", "20"]
    var1 = int(var[0])
    var2 = int(var[1])

    #if, elif, else. ...
    ```
