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

