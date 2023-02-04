---
title: Python basic day4
categories: [programming, Python]
tags: [python, basic, programming]
date: 2022-08-13 04:15:00 +0900
---

# 1. 복습
```python
a = [1,2,3,[1,2,3]] # list 정의
print( a[1] )  # indexing
print( a[2:3] ) # slicing
```

# 2. 수업
- list는 코테(코딩테스트)에서 많이 활용됨
- 코딩테스트 = 알고리즘 테스트 (하나의 결과를 최소한의 시간에 출력하게끔 코딩하는 테스트)
## 2-1) List 형태의 method 설명
- 호출방식: list형태의 변수.메서드이름( 인자값)
- method 종료 확인하는 방법
  ```python
  var1 = []
  print( dir(var1) ) 
  # 결과: ['__add__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
  ```
## 2-2) List 형태의 method 종류
- append( 변수명 )
  - 특정한 값 하나를 list 변수에 추가하는 method이다.
  - 예시
    ```python
    var1 = []
    test = 1

    var1.append( test ) # append: 값을 추가하기 위한 메서드
    var1.append( 2 )
    var1.append( "test" )
    var1.append( [3,4,5,6] )
    ```
- pop()
  - list에서 가장 오른쪽에 있는 값을 빼내오는 method이다.
  - 예시
   ```python
   # var2 = var1.pop() # pop: 가장 우측에 있는 값을 빼는고 return 값으로 반환한다.
   # [1, 2, 'test', [3, 4, 5, 6]] <-- 시작 후 pop
   # [1, 2, 'test'] <-- 또 pop()
   # [1, 2]
   var1 = [1, 2, 'test', [3, 4, 5, 6]]
   print( var1 )
   print( var1.pop() )
   print( var1 )

   [result]
   [1, 2, 'test', [3, 4, 5, 6]]
   [3, 4, 5, 6]
   [1, 2, 'test']
   ```
- remove( 변수명 )
  - 특정한 값을 지우는 method이다.
  - 예시
   ```python
   var1 = [1, 2, 'test', [3, 4, 5, 6]]
   var1.remove( 'test' )   # 지정된 값을 지우는 method
   print( var1 )
   ```
- clear()
  - list 변수를 깨끗하게 비워주는 method
  - 예시
    ```python
    var1 = ['a','b','c']
    var1.clear()
    ```

- copy()
  - list의 값만 복사를 해준다.
  - 예시
    ```python
    var1 = ['a','b','c']
    var2 = var1.copy()  # var2 = var1
    ```

- count( 값)
  - 지정된 list에 인자로 전달한 값이 몇개인지 출력(return)해준다.
  - 예시
    ```python
    var1 = ['a','b','c','a','a']
    print( var1.count( 'a' ) ) 
    print( var1.count( 'b' ) ) 
    print( var1.count( 'c' ) ) 
    ```

- extend( list_형태의_변수 )
  - 지정된 list에 인자로 전달한 값이 몇개인지 출력(return)해준다.
  - 예시
    ```python
    var1 = [1,2,3]
    var2 = [7,8,9]
    var1.extend( [4,5,6] )  # 배열의 확장
    var1 = var1 + var2 # extent 기능과 동일..
    ```

- reverse()
  - 지정된 list를 역순으로 나열한다.
  - 예시
    ```python
    var = [1,2,3,4,5]
    var.reverse()
    print( var )    # 출력결과: [5,4,3,2,1]
    ```
    
- sort()
  - 지정된 list를 오름차순(1,2,3,..) 으로 나열해준다.
  - 예시
    ```python
    var2 = [3,1,4,2,5]
    var2.sort()
    print(var2) # 출력결과: [1,2,3,4,5]
    ```
   
## 2-2) Type: Dict
 - 정의하기
   ```python
   a = {
       "apple": '사과입니다.',
       "banana": '바나나',
       'c': 1,
       'd': 2,
       'e': 3
   }
   ```
 - 원하는 key에 맵핑된 value를 읽어오기
   ```python
   print( a )
   print( a["banana"] )    # list 보다 값을 빨리 찾을 수 있음
   print( a["asfasdfasdf"] )   # KeyError: 'asfasdfasdf'
   ```
 - 비어있는 dict에 새로운 key를 추가할떄
   ```python
   var = {}    # 비어있는 dict 선언
   print(1, var)
   #var["key_name"] = "value"
   var["iphone"] = "아이폰13 미니 프로입니다."
   var["iphone2"] = "아이폰14 미니 프로입니다."
   var["iphone"] = "아이폰15 미니 프로입니다."    # key 추가시 주의!! 동일한 key가 있을때 다시 값을 넣으면 기존 값은 지워지고 새로운 값이 추가가 됨
   print(2, var)
   ```
 - 원하는 key를 제거하거나 변수를 제거할 때
   ```python
   del var["iphone"]  # << 원하는 key를 제거할때 변수 앞에 'del' 을 작성해준다.
   print(b)

   # [참고]
   del b  # << 변수 자체를 제거할때, b라는 변수 자체가 없어짐. **에러주의**
   print(b) # 바로 윗줄에서 del 했기 때문에, "NameError: name 'b' is not defined"라는 에러 발생
   ```

# ToDo
1. 함수와 return에 대하여 짧게 배웠는데, 다음 [함수] chapter에서 본격적으로 다루기
2. list와 dict 한번씩 따라해보면서 이해하기
3. 숙제 (1)
    - #1-1) 사용자에게 5가지 숫자를 입력받고 list 변수에 추가한다.
    - #1-2) list 변수를 [정렬한 list] 와 [역순 list]를 각각 출력한다.
    - #1-3) list에 있는 모든 값을 제거하여 비어있는 list로 만든다.
4. 숙제 (2)
    - #2-1) 비어있는 dict타입의 변수를 만든다.
    - #2-2) 5쌍의 key:value를 비어있는 dict타입 변수에 추가한다.
    - #2-3) key를 참조하여 value를 출력하도록 한다.