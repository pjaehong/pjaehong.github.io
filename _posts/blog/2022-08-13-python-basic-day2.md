---
title: Python basic day2
categories: [programming, Python]
tags: [python, basic, programming]
date: 2022-08-13 04:09:00 +0900
---
# 1. 복습
- 변수선언
    ```python    
    nuber1 = 10
    nuber2 = 3
    ```
- 숙제(계산기 코드) 검토

# 2. 수업진행
- 수치 연산자
    ```python
    # number1 = 10
    # number2 = 3
    # >>> 10 + 3 = 13 
    print( nuber1 + nuber2 )
    print( nuber1 - nuber2 )
    print( nuber1 * nuber2 )
    print( nuber1 / nuber2 )
    print( "========" )
    print( nuber1 // nuber2 )   # 몫
    print( nuber1 % nuber2 )    # 나머지
    print( "========" )
    print( nuber1 ** nuber2 )   # 제곱근 -> 10 ** 3
    # 숙제1) 숫자 2개를 입력 받고, +,-,*,/ 연산 결과를 출력하는 코드를 짜주세요.
    ```
- 비교 연산자 (코딩에서 조건문[if,elif,else] 코딩시 사용됨)
    ```python
    n = 10
    m = 3
    print( n > m )  # 이 비교한 결과가 참(True), 또는 거짓(False) 인지 결과를 보여줌
    print( n < m )
    print( n >= m )
    print( n <= m )
    #a = 123 # 대입연산자
    #n = m   # 대입연산자
    print( n == m ) # 두 값이 '같은지' True or False
    print( n != m ) # 두 값이 '다른지' True or False
    ```
- 논리 연산자
   - and: 2 개 이상의 조건에서 모든 조건이 True 일때만 결과는 True이다.
   - or : 2 개 이상의 조건에서 단 하나의 조건이라도 True이면 결과는 True이다.
        ```python
        n1 = 2
        n2 = 2
        n3 = 30
        n4 = 40
        print( n1 == n2)
        print( n3 < n4 )

        #if (n1==n2) or (n3 < n4):
        #if ((n1 == n2) or (n1 == n3)) and (n1>n3) .... :
        if (n1 == n2) and ( n3 < n4 ):  # True and False
            print( 'ok' )
        ```
   - not: 반대의 값을 결과로 보여줌.단, 여기서 반대라고 함은 ( 0(False) <-> 1(True) )
        ```python
        a = True  # 사람이 봤을때 123 , "test" -> 컴퓨터: 000000000000000000000001  << 1이 단 하나라도 잇으면 이것은 True..
        print( not a )  # False
        b = False
        print( not b )  # True

        a = 123 # 0이 아닌 어떤 값이므로 True -> not a -> False
        b = 0   # False -> not b -> True
        c = None # False -> not b -> True
        print( not a )
        print( not b )
        print( not c )
        # in, not in은 list 타입을 배울 때 같이 진도나가기.
        # `bit연산자`는 참고용으로 URL 공유하기 (암호학, 수식을 요구하는 개발할때 활용 많이함)
        ```
- 객체 비교 연산자
    ```python
    var1 = 123  # int     -> 1111011
    var2 = "123"    # str -> 1글자당 1byte..1byte는 8bit, 1bit가 0 또는 1로 나타나지는 단위  
                    # 00110001  00110010  00110011
    print( type(var1) ) # type: 변수의 형태를 출력해준다.
    print( type(var2) )

    print( var1 == var2 )   # 단순히 값만 비교
    print( var1 is var2 )   # 객체(?)(또는 type)을 비교
    print( var1 != var2 ) 
    print( var1 is not var2 ) 
    ```
   
# 3. 다음 수업시간
- 나머지 시간에 python진도 (Dict, List)