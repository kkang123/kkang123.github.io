---
layout: post
title: 파이썬 for beginner 자료구조와 알고리즘 2장 연습문제
tags: [python]
categories: practice problem
---

# 파이썬 for beginner 자료구조와 알고리즘 2장

## 1. 다음 중 파이썬의 데이터형이 아닌 것을 모두 고르시오.  
`short, bool, long, int, double, float, char, str`  
```python
#short, long, char -- c언어
```

<br>

## 2. print() 함수에서 사용할 수 있는 서식  
정수 %d  
실수 %f  
문자열 %s  
문자 %c  
(%d, %x, %o = 10진수, 16진수, 8진수)
    
<br>  

## 3. 설명에 해당하는 함수 이름 채우기
`input()` 함수는 값을 입력받는데 사용된다. ~~~~~ 모든것을 문자열로 입력받기 때문에 숫자로 입력을 원한다면  `변수 = int(input())`

## 4. 산술연산자   
몫만 남긴다. //  
나머지만 남긴다. %  
제곱을 계산 **  

## 5. 종류가 다른 연산자  
`== 같다`  
`!= 같지않다`  
`> 크다`  
`+= 대입연산자`  
`< 작다`  
`>= 크거나 같다`  
`<= 작거나 같다`

## 6. 조건문 결과 예측
```python
a = 200
if a < 100:
    print("100보다 작군요.")
```  
아무것도 출력 안됨
(001.py)
```python
a = 200
if a < 100:
    print("100보다 작군요.")
else:
    print("a가 크군요")
```
## 7. 반복문  
```python
for i in range(1, 10, 1): #1부터 9까지 1씩 증가
    # 이 부분 반복
```
9번  
(002.py)
```python
for i in range(1, 10, 1): #1부터 9까지 1씩 증가
    print('%d'% i)
```
## 8. while문 'ㅎ' 출력 갯수 예상  
```python
while True:
    print("ㅎ", end = " ")
    break
```
한번 (break문 때문)  
(003.py)  
```python
while True:
    print("ㅎ", end = " ")
    break
```
## 9. 함수 선언과 함수 호출 채우기
```python
def addValue(v1, v2):
    result = 0
    result = v1 + v2
    '1'return result

hap = '2'addValue(100, 200)
print("100과 200의 addValue() 함수 결과는 %d" % hap)

#' '빈칸 부분
```    
(004.py)
```python
def addValue(v1, v2):
    result = 0
    result = v1 + v2
    return result

hap = addValue(100, 200)
print("100과 200의 addValue() 함수 결과는 %d" % hap)
```
## 10. 코드의 실행 결과 예상
```python
def func1():
    var = 100
def func2():
    global var
    var = 200

var = 0
func1()
print(var)
func2()
print(var)

#출력
'''
0
200
'''
```
(005.py)
```python
def func1():
    var = 100
def func2():
    global var
    var = 200

var = 0
func1()
print(var)
func2()
print(var)
```
## 11. 코드의 결과에서 리스트 크기는?
```python
lst = []
for i in range(0, 200):
    lst.append(0)
len(lst)

#200
```
(006.py)
```python
lst = []
for i in range(0, 200):
    lst.append(0) #리스트 항목을 0으로 채워줌
print(len(lst))
```
## 12. 코드 출력 값
```python
aa = [ 10, 20, 30, 40]
print(a[0])
print(a[-1])
print(a[1:3])
print(a[2:])

#변수명이 달라 출력 안됨
#올바르면
'''
10
40
[20, 30]
[30, 40]
```
(007.py)
```python
aa = [ 10, 20, 30, 40]
print(aa[0])
print(aa[-1])
print(aa[1:3])
print(aa[2:])
```
## 13. 리스트 조작 함수  
리스트에서 해당 값의 개수를 센다  
count()  
지정한 값을 찾아 위치를 반환  
index()
리스트 내용을 새로운 리스트에 복사  
copy()  
리스트 맨 뒤의 항목을 빼낸다  
pop()

## 14. 코드의 결과 예상
```python
dataList = [data for data in range(1, 10) if num % 4 == 0]
print(dataList)

# num을 data로 변경
```
(008.py)
```python
dataList = [data for data in range(1, 10) if data % 4 == 0]
print(dataList)
```
## 15. 딕셔너리 특성
1. 중괄호 {}로 구성
2. 키와 값의 쌍으로 구성
3. 읽기 전용이다 (튜플)
4. 키는 중복될 수 (없다)

## 16.set세트의 특성
1. {}을 사용하지만 :는 없이 값을 입력
2. 딕셔너리에서 값이 아닌 키만 모아 놓은 형태이다(중복되는 것은 자동으로 사라진다)
3. 읽기 전용은 튜플
4. 중복된 값은 존재하지 않는다.

## 17. 다음 코드의 결과 예상
```python
myStr = '#'
myStr.join('IT쿡북')
print(myStr)

#출력
#
```
(009.py)
```python
myStr = '#'
myStr.join('IT쿡북')
print(myStr)
```
## 18. 튜플 특성
1. 소괄호로 ()로 구성되어 있다.
2. 리스트처럼 tup[3]형태로 접근 가능
3. 읽기전용이지만, append()함수를 사용하여 데이터를 추가할 수 없다.
4. 읽기 전용이므로 del(tup)처럼 튜플 자체를 삭제하려고하면 오류가 발생한다.?는 틀린 말 삭제 가능
