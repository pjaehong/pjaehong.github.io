---
title: Python basic day3
categories: [programming, Python]
tags: [python, basic, programming]
date: 2022-08-13 04:12:00 +0900
---

# 1. 복습
```
num1 = "100"
num2 = "30"
print( f"{num1} + {num2} = {int(num1) + int(num2)}")
```

# 2. 컴퓨터 이론
## 1) 메모리
   ```python
    a = 100 # ---> com: 11101110111000
    b = 200 # ---> com: 00101110110111   => memory 할당(allocate) .. => 각 변수는 메모리의 특정 address(주소..)에 저장됨을 의미한다.
    c = b   # b에 대한 속성(객체, 타입 등) 을 그대로 c에 할당

    print( hex(id(a)), a ) # a 의 메모리 주소 출력
    print( hex(id(b)), b ) # b 의 메모리 주소 출력
    print( hex(id(c)), c ) # b 의 메모리 주소 출력

    [result]
    0x100ee55d0 100
    0x100ee6290 200
    0x100ee6290 200
   ```
## 2) 객체지향
### 2-1) 절차지향 프로그래밍(feat. 함수 개념만 대충)
- 소스코드 상단부터 하단까지 순차적으로 실행됨
- 순차적으로 실행되면서 조건문, 반복문, 함수들을 수행하며 다른 분기로 빠짐
- 예제
   ```python
    def handle():
        print( "이것은 핸들입니다." )

    def door():
        print( "이것은 문입니다." )

    def door2():
        print( "이것은 문2입니다." )

    handle() # 함수를 호출한다.
   ```
   
### 2-2)  객체 개념만 대충.. (class)
- 객제로 존재하는것, 사물 또는 개념이며 객체가 가진 기능과 속성에 따라 용도가 다르다.
- 위의 개념을 프로그래밍에 접목시킴
- 예제
   ```python
    class car():
        def __init__( self ):
            return
        def self.handle( self ):
            print( "이것은 핸들입니다." )

        def self.door( self ):
            print( "이것은 문입니다." )

        def self.door2( self ):
            print( "이것은 문2입니다." )
    var = car()
    var.handle()
   ```

- 참고
   - 객체지향을 사용하는 웹개발 언어
   - NodeJS, Typesciprt, php, jsp, ...

# 3. list 타입이란
- 다양한 값을 하나의 변수에 나열할 때 사용됨
- 하나의 list 타입에는 다양한 형태로 나열해도 무관함( [1,2,3,4], ['a','b',c'], [1,'test2', 3, [1,2,3]] )
- 예제
   ```python
    a = 1
    b = 100
    c = "123"
   ```
- list의 길이 확인
   ```python
   var1 = [ 1, 2, 3, 4, "test1", "test2", ['a','b','c']]
   print( "var1의 길이는 {} 입니다.".format(len(var1)) )   # 길이
   ```
- Indexing ( n 번째 위치에 대한 값을 출력하기 위함)
   ```python
    var1 = [ 1, 2, 3, 4, "test1", "test2", ['a','b','c']]
    print( var1[0] )    # 1
    print( var1[1] )    # 2
    print( var1[2] )    # 3
    print( var1[6] )
    print( var1[6][2] )
    print( var1[-1] )
    print( var1[-2] )
   ```

- Slicing( n ~ m까지 출력하기 위함)
   ```python
    print( 1, var1[3:])    # n 부터 끝까지 출력
    print( 2, var1[6:])    # n 부터 끝까지 출력
    print( 3, var1[:3])    # m 부터 끝까지 출력
    print( 4, var1[:4])    # m 부터 끝까지 출력
    print( 5, var1[3:6])   # 3 ~ 6까지 출력

    print( 6, var1[-3:])    # -3번째부터 list의 끝까지
    print( 7, var1[:-3])    # 처음부터 -3번째까지 출력
   ```
- 참고: 문자열에서도 index와 slice 개념 적용됨
   ```python
    _str = "HELLO"
    print( _str[0] )
    print( _str[1] )
    print( _str[-1] )
    print( _str[1:3:2] )
   ```

# 4. ToDo
- List의 method 알아보기
- dict 타입 진도나가기