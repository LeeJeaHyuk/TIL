# Join

inner join

컬럼명은 같아도 되고 달라도 된다 / 비교하는 컬럼의 같은 값을 추출한다

각 테이블의 조인 컬럼을 비교하여 조인조건을 만족하는 레코드만 선택하는 조인

```sql
-- ANSI
FROM M JOIN S ON (M1 =S1);

FROM M INNER JOIN S ON(M1=S1)

-- ORACLE
FROM M,S WHERE M1 = S1;
```

ANSI가 WHERE절이 늘어날수록 편하다



USING : 조인테이블의 같은 컬럼명

ON : 조인테이블에 다른 컬럼명



```sql
FROM A JOIN B JOIN C USING(RES)
```



## CROSS JOIN

각 테이블의 모든 로우에 대해서 가능한 모든 조합을 가지는 쿼리 결과를 만들어 내는 조인



```sql
-- ANSI JOIN
SELCET *
FROM M CROSS JOIN S

-- SQL SERVER JOIN
SELECT *
FROM M,S

```



## OUTER JOIN

두 테이블 간 주, 종 관계를 두고 주 테이블의 모든 레코드와 종 테이블에서 조인 조건을 만족하는 레코드만 가져올 때 사용

주 테이블의 위치에 따라서 LEFT OUTER JOIN, RIGHT OUTER JOIN, 그리고 두 개의 결과를 합한 FULL OUTER JOIN으로 구분됨



### LEFT OUTER JOIN





# 9/27일까지 정리

Python

기본자료형 / 연산자 / 제어문 / 함수 [고차함수] / 클래스 / 상속 / 다형성 / 파일 입출력 / os, sys 등 모듈

map reduce zip

삼성아카메디 알고리즘



ORACLE

select / where(조건문) 연산자 / 집계함수를 통한 group by / having / order by / rollup , cube, group, grouping set / 서브쿼리 / 조인 / 데이터무결성 (제약조건) / 테이블CRUD / 시퀀스 / view, index / pl/spl / 함수 프로시저 트리거



