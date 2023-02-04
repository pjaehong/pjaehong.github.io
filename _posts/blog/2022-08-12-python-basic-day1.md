---
title: Python basic day1
categories: [programming, Python]
tags: [python, basic, programming]
---
# 0\. ToDo
- 변수 정의 (데이터 타입: string, integer, float,// list, ...)
- 사용자 입력/출력 (input, print)

# 1\. 변수 정의
- 기본 형태
  ```python
  number1 = 1 # 기본 형태
  number2 = 123.0
  string = "test1"
  print( string ) # 출력하는 기능
  print( number1 )
  print( number2 )
  ```
- 실습: test 변수에 100을 입력하고, 그 값을 출력하시오
- 변수명 규칙
   ```
   # 변수명 정의 규칙
    # 1. 특수문자는 변수명으로 사용할 수 없다.
     -> number! = 123

    # 2. 변수명 첫번째 글자는  영문자 (소문자 or 대문자)), 또는 언더바(_) 사용가능
     -> Number = 123
     -> number = 123
     -> 1number = 123
     -> $number = 123
     -> _number = 123

    # 3. 변수명에는 영문 소,대,숫자, _ 사용가능
     -> number1 = 123
     -> Number1 = 123
     -> number_1 = 123
     -> _number1 = 123
   ```
- Tip: 변수명 정의 시, 해당 변수의 역할을 알 수 있도록 작성하기.
   ```python
    IntNumber1 = 10 #a = 10
    IntNumber2 = 20 #b = 20
    print( IntNumber1 + IntNumber2 )
   ```
   

# 2\. 데이터 출력 (print())
- 컴퓨터 화면에 데이터가 출력되는 기능
- print 출력 방법 (여러 개)
   ```python
  number = 100    # integer
  number2 = "200" # string
  number3 = 300 

  print( number )
  print( "입력한 값은 ", number, number2 )    # 출력하고 싶은 변수나 문자를 ,를 기준으로 나열하기
  print( "입력한 값은 %f %s %d" % ( number, number2, number3 ) )    # 형식 지정자로 출력 
  print( "입력한 값은 {0} {1} {2}".format(number, number2, number3) )
  print( f"입력한 값은 {number} {number2} {number3}")
  print( "'Test 1'" )
  print( "\"Test 2\"" )   # 특수문자 앞에는 역슬러시(\)를 입력해준다.
   ```
# 3\. 데이터 입력 (input())
- 사용자가 컴퓨터로 입력하는것
- 예시
   ```python
  input_data = input( "채팅을 입력하세요: " )
  print( "입력한 데이터는 {0} 입니다.".format(input_data) )
   ```
- input() 형태는 무조건 string이다. (형태를 변환하기 위해서는 typecasting을 해준다.)
   ```python
  # input()으로 받은 데이터는 무조건 string 형태이다.
  number1 = input( "1st num: " )
  number2 = input( "2nd num: " )
  print( number1, number2 )
  print( number1 + number2 )  # string 형태에 +를 사용하면 두개의 문자열이 붙는다.
  print( int(number1) + int(number2) ) # 형변환(형태변환, type cast) , int(): str to int
  print( float(number1) + float(number2) )
   ```
   ```python
  string = 100
  string2 = 200
  print( string + string2)
  print( str(string) + str(string2) ) # str(): int to string
   ```

# 4\. 주석
- 타입1
  ```python
  # 주석: python 코드에서 실행되지 않고, 개발자가 메모용 또는 설명용으로 넘기기 위한 멘트
  # #을 입력하면 한줄씩만 주석처리됨
  ```
- 타입2
   ```python
  '''
  여러 줄을 주석처리 하고 싶으면
  주석을 시작할때 싱글쿼터(') 를 3개 연달아 쓰고,
  주석을 종료할때도 싱글쿼터(') 를 3개 연달아 쓴다.
  '''
   ```

# 5\. 숙제
  - 사용자한테 4개의 입력을 받고, 이 값들을 각 4개의 변수에 저장을 한다.
  - 각 변수를 출력할 때는 형태가 다른 print() 로 출력하는 코드를 짜세요
