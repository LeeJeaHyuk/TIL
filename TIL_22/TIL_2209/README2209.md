# TIL (220922~220928)

## Day 1 start (220922)

1. 폴더, 파일 생성, 이동 삭제
2. 파일 조회 , 열기
3. 간단한 markdown 
4. git
   - log  ,diff
   - clone, remote
   - push
5. **branch 관련 추가 요망**

## Day 2 220923

## Day 3 220924

## Day 4 220926

## Day 5 220927

## Day 6 220928

orcle 프로시저 함수





### numpy , pandas

---

### Series 

자료구조 인덱싱 객체 생성

인덱스 문자열로 지정해주어도 숫자로 추출 가능

슬라이싱으로 추출 

```python
s[[1,3]]
s[1:3]
```







---



seeborn을 사용한 titanic dataset으로 dataframe 학습

데이터 확인 

출력

---



# Day 7 220929

### pandas 데이터처리 및 변환

- count()
  - 시리즈에서 데이터 개수를 셀 수 있다 count() 7-1
  - 데이터프레임에서 개수를 셀 수 있다 count() 7-2

- 난수를 발생시킬 수 있다 7-3 
  - np.random.randint, seed,time
  - 고정된 난수 발생
- value_count
  - 카테고리 값을 셀 수 있다 value_counts() 7-4
    - 시리즈의 값이 정수 문자열 등 카테고리 값인 경우
  - 범주형 데이터 7-5
    - 범주형 데이터에 value_counts() 사용
  - 데이터프레임에 value_counts() 사용 7-6
- sort 정렬 7-7
  - sort_index()
  - sort_value()

---

# Day 8 220930

csv파일 읽어오기

