
# PYTHON 

# 문자열, 숫자, 형변환 메소드

1. 문자열메소드
    * a.startswith('b'), a.endswith('b')
    * a.find('b'), a.rfind('b')
    * a.count('b'), len(a)
    * a.lstrip(), a.rstrip(), a.strip #공백제거
    * a.isalpha(), a.isnumeric(), a.isalnum() #True/False 리턴
    * a.replace('a', 'b') #a를 b로 변경
    * a.split(',') #a를 지정문자를 기준으로 리스트만듬★
    * ','.JOIN(a) #지정문자를 기준으로 리스트 a를 합침★
    * a.lower(), a.upper()
    * 문자열{}.format(대입값) // print(문자열%s %d, %(대입값))
    * a.tilte() #단어별 첫글자 대문자
    * a.capitalize() #전체의 첫글자 대문자 나머지 소문자
    * a.swapcase()   #대소문자변경
    * a.center(자리수), a.center(자리수, 문자)  #가운데정렬, 빈곳은 해당문자로 채움
    * a.ljust(자리수, 문자), a.rjust(자리수, 문자)
2. 숫자 메소드
    * a, b = divmod(5,3) #a에는 몫, b에는 나머지
    * abs(-4), round(4.1), math.trunc(4.1)  #import math
3. 형변환
    * int() 숫자, float() 실수
    * complex() 복소수, str() 문자
4. 진법
    * bin() 2진법, oct() 8진법, hex() 16진법

# 문자열 문제

문자열 v_str = "시간은 멈추지 않습니다. 하루를 유익하게 살아야합니다."
문제 3
1. "시간은 멈추지 않습니다." 만 출력해주세요


```python
v_str = "시간은 멈추지 않습니다. 하루를 유익하게 살아야합니다."
```


```python
v_str[:13]
```




    '시간은 멈추지 않습니다.'



2. "하루를 유익하게 살아야합니다." 만 출력해주세요


```python
v_str[14:]
```




    '하루를 유익하게 살아야합니다.'



3. "살아야합니다."  만 출력해주세요


```python
v_str.find('살아야')
```




    23




```python
v_str[23:]
```




    '살아야합니다.'



4. "시추니루하야"  이 글자만 출력해주세요.


```python
v_str[::5]
```




    '시추니루하야'



5. "시간은 멈추지 않습니다. 하루를 유익하게" 만 출력해주세요.


```python
v_str[0:22]
```




    '시간은 멈추지 않습니다. 하루를 유익하게'



6. v_str 문자열을 뒤순으로 출력해 주세요.


```python
v_str[::-1]
```

문제 4. 포맷문자를 이용해서 출력하세요.

1. 안녕하세요. {제임스} 입니다. 즐겨듣는 음악은 {클래식} 입니다.


```python
'안녕하세요.{}입니다. 즐겨듣는 음악은 {}입니다.'.format('제임스','클래식')
```


```python
print('안녕하세요, %s입니다. 즐겨듣는 음악은 %s입니다.'%('제임스','클래식'))
```


```python
name = '제임스'
music = '클래식'
print('안녕하세요. {}입니다. 즐겨듣는 음악은 {}입니다.'.format(name, music))
```

    안녕하세요. 제임스입니다. 즐겨듣는 음악은 클래식입니다.
    

2. {996} 를 {8} 나누면 {124}는 몫이고 {4} 나머지입니다


```python
num_1 = 996
num_2 = 8
result_1,result_2 = divmod(num_1,num_2)   #이때 몫은 result_1, 나머지는 result_2에 저장됨
print('%d 를 %d 나누면 %d는 몫이고 %d나머지입니다'%(num_1,num_2,result_1,result_2))
```

    996 를 8 나누면 124는 몫이고 4나머지입니다
    

문제5
1. 반복문을 사용하지 않고  * 를 가로 100개 출력


```python
'*'*100
```




    '****************************************************************************************************'



2. 반복문을 사용하지 않고  * 를 세로 10개 출력


```python
print('''*
'''*10)   #'줄띄움 가능single qutation mark 3개
```


```python
print('*\n' * 10) #줄바꿈 \n
```

3. alha = 'aAbBcCdDeEfFgGhHiIjJkK' 변수에 값이 들어 있습니다. 
화면의 결과는  ABCDEFGHIJK 출력하세요.


```python
alha = 'aAbBcCdDeEfFgGhHiIjJkK'
```


```python
alha[::-2][::-1]
```


```python
print(alha[1::2])
```

문제6
a = 'a b c d e f g' 변수에 문자열이 들어 있습니다. 다음을 수행하세요.

1. a 변수에 있는 문자의 갯수를  구하세요.


```python
a = 'a b c d e f g'
```


```python
len(a)
```

2. a 변수에 공백문자 갯수를 구하세요.


```python
a.count(' ')
```

3. a 변수 안에 있는 공백문자를 제외한 갯수를 구하세요.


```python
print(len(a) - a.count(' '))
```

4. a 변수에 있는 공백문자를 제거한 후 b 변수에 넣어주세요


```python
b = a.replace(' ','')
b
```




    'abcdefg'



5. a 변수에 있는 문자를 분리한 후 c 변수에 넣어주세요.


```python
c = a.split(' ')
c
```




    ['a', 'b', 'c', 'd', 'e', 'f', 'g']



6. c 변수에 있는 문자를 합쳐서 자신의 변수에 다시 넣어주세요.


```python
c = ','.join(c)
c
```




    'a,b,c,d,e,f,g'



# 데이터 자료형(list, tuple, set, dictionary, range)

## 1. list   (a = [ , , , ])
- 다른 자료형(숫자, 문자등) 한 리스트에 담을 수 있음
- 방번호(index)는 자동으로 설정됨
- [ ] + [ ] 리스트끼리 결합가능
- 리스트 메소드 (삽입, 삭제, 정보 출력, 정렬)
    * a.append('값'), a.extend([값1, 값2,..]), a.insert(방번호, 값)   #다중 값, 방번호지정 등의 값 삽입가능
    * a.remove(값), a.pop(값), del a[방번호]   #해당 인덱스의 값 삭제 가능
    * a.index(값), a.count(값), len(a)   #값에 대한 인덱스출력, 값에 대한 건수출력, 전체건수 출력
    * a.sort(reverse = True 옵션), a.reverse()   #값 정렬, 자기자신에게 소트결과넣음
    * 변수 = sorted(a, reverse = False) #정렬후 객체저장가능(얘는 함수임)
    * for x, y in enumerate(a)  #각 반복시 변수에 대한 인덱스, 값추출가능
- 리스트 내장객체
    * 리스트변수 = [i표현식 for i in 변수]
    * 리스트변수 = [i for i in 변수 if 조건식]
   
## 2. tuple   (a = ( , , ))
- 읽기전용! 따라서 수정불가능 read-only
- 방번호 자동설정
- ( ) + ( ) 튜플끼리 결합가능
- 요소 1개시 , 넣어야함
- ★패킹, 언패킹 가능 (튜플요소 수 일치)
- 튜플 메소드 (정보출력)
    * a.index(값), a.count(값)
    
## 3. set   (a = { , , })
- 집합계산시 유용
- 인덱스 없음, 중복 불허!
- 셋 메소드
    * a.union(b)  # a|b합집합, a.intersection(b)   # a&b교집합
    * a.difference(b)   #a-b차집합
    * 값 in a, a = set() #선언!딕셔너리와 구별
    * a.add(값), a.remove(값)
 
## 4. dictionary  (a = {'키1': '값1', '키2' : 값2', '키3':'값3})
- key와 value값으로 이루어짐
- 키밸류 한 묶음씩 튜플로 언패킹 가능 ; 변수1, 변수2 = dic.items()
    * a = {} #선언
    * a['키1'] = '값1' #키 값을 이용한 데이터 삽입
    * del a['키'], dic.pop('키')   #키 값을 이용한 데이터 삭제
    * a.clear()   #a안 데이터전체삭제
    * a.items(), a.keys(), a.values(), 값 in a.keys(), 값 in a.values()
    * for x, y in dic.items()   #키값과 밸류값 추출가능
- 소트 : 키값/ 밸류값을 기준으로 소트시 operator 모듈이용(타입바뀜)
    * res_sort = sorted(res.items(), key = operator.itemgetter(0))
    * 0 은 키 / 1은 밸류

## 5. range
- 반복문에서 많이 쓰임
- range(끝)  ★주의 : 끝포함 X
- range(스타트, 끝)
- range(스타트, 끝, 증가값)
    * range(10)   # 0부터 9까지
    * range(2, 10, 2)  # 2 4 6 8


```python
a = [1,2,3]
```


```python
a,b,c = a #언패킹
```


```python
a = a,b,c #패킹
```


```python

```




    int



문제 7
food = [['김밥','라면','오뎅'],['비빔밥','김치찌게'],['자장면','짬뽕']]
1. 1번 index에 청국장 추가 하세요


```python
food = [['김밥','라면','오뎅'],['비빔밥','김치찌게'],['자장면','짬뽕']]
food[1].append('청국장')
```

2. 2번 index에 탕수육 추가하세요.


```python
food[2].append('탕수육')
```

3. 0번 index에 있는 오뎅 삭제하세요.


```python
food[0].remove('오뎅')
```

4. 0번 index에 튀김, 튀김, 떡복이 한꺼번에 추가하세요


```python
food[0].extend(['튀김','튀김','떡복이'])
```

5. 2번 index에 2번 위치에 유산슬 추가하세요


```python
food[2].insert(2,'유산슬')
```

6. 튀김이 갯수를 세어주세요


```python
 food[0].count('튀김')
```

7. 0번 index만 정렬해주세요


```python
food[0].sort()
```


```python
food.sort()
```


```python
food.sort(reverse = True)
```

8. 0번 index에 마지막 데이터 삭제하세요


```python
food[0].pop()
```
