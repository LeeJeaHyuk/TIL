- count()
  - 시리즈에서 데이터 개수를 셀 수 있다 count() 7-1
  - 데이터프레임에서 개수를 셀 수 있다 count() 7-2



- 난수를 발생시킬 수 있다 7-3 

  ```python
  import time
  print(time.time())
  np.random.seed(int(time.time()))
  np.random.randint(5, size=4)
  ```

  

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

- df.sort_values() : 특정열 값 기준 정렬
    - 데이터프레임은 2차원 배열과 동일하기 때문에
        - 정렬시 기준열을 줘야 한다. by 인수 사용 : 생략 불가
        - by = 기준열, by=[기준열1,기준열2]
    - 오름차순/내림차순 : ascending = True/False (생략하면 오름차순)
- df.sort_index() : DF의 INDEX 기준 정렬
    - 오름차순/내림차순 : ascending = True/False (생략하면 오름차순)



sort index

**Series.****sort_index****(***axis=0***,** *level=None***,** *ascending=True***,** *inplace=False***,** *kind='quicksort'***,** *na_position='last'***,** *sort_remaining=True***,** *ignore_index=False***,** *key=None***)**

**kind****{‘quicksort’, ‘mergesort’, ‘heapsort’, ‘stable’}, default ‘quicksort’**

​	

```
s2.sort_index(ascending = False)
s2.sort_values(ascending = False)
```



dataframe

```python
```

인덱스 바꾸기 df.index=['aa','bb','cc','dd'] df,Series 모두 가능



데이터프레임에서 중앙값 최소값 최대값을 추가할 수 있다