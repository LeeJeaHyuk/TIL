![image-20220928104459347](../../images/TIL_day05_220928wen/image-20220928104459347.png)

SQLPLUS/SCOTT/scott1234

sqlplus/계정/비번

![image-20220928105422381](../../images/TIL_day05_220928wen/image-20220928105422381.png)



GETSAL FUNC



```sql
CREATE OR REPLACE FUNCTION getSal
(
  P_EMPNO IN EMP.EMPNO%TYPE 
) RETURN number AS 
   v_sal emp.sal%type; 
   v_tot number :=0; -- 초기화
   begin   
   select sal into v_sal from emp
   where empno = p_empno;      -- 사원번호에 해당하는 부서번호출력
   
   v_tot := v_sal*12;
   RETURN v_tot;
END getSal;
```

![image-20220928110351921](../../images/TIL_day05_220928wen/image-20220928110351921.png)

![image-20220928110449122](../../images/TIL_day05_220928wen/image-20220928110449122.png)



getBong

```sql
CREATE OR REPLACE FUNCTION GETBONG 
(
  P_EMPNO IN EMP.EMPNO%TYPE 
) RETURN number AS 
   v_sal emp.sal%type; 
   v_comm EMP.COMM%type;
   v_tot number :=0; -- 초기화
   begin   
   select sal,comm into v_sal, v_comm
   from emp where empno = p_empno;      -- 사원번호에 해당하는 부서번호출력
   
   v_tot := v_sal*12+nvl(v_comm,0);-- nvl()
   RETURN v_tot;
END GETBONG;

```

nvl로 null 처리



# 뷰

[ VIEW ]
  : 다른 테이블이나 뷰에 포함된 맞춤표현(virtual table)
    join하는 테이블의 수가 늘어나거나 질의문이 길고 복잡해지면 작성이 어려워지고
    유지보수가 어려울수 있다. 이럴때 스크립트를 만들어두거나 stored query를 사용해서
    데이터베이스 서버에 저장해두면 필요할때 마다 호출해서 사용할수 있다

   - 자체적으로 데이터를 포함하지 않는다
   - 베이스테이블(Base table) : 뷰를 통해 보여지는 실제테이블
   - 선택적인 정보만 제공 가능

[형식]
create [or  replace] [force | noforce ] view  뷰이름 [(alias [,alias,.....)]
as 서브쿼리
[with check option [constraint 제약조건이름]]
[with read only [constraint 제약조건이름]]

  - create or replace : 지정한 이름의 뷰가 없으면 새로생성,동일이름이 있으면 수정
  - force | noforce
          force   : 베이스테이블이 존재하는 경우에만 뷰생성가능
          noforce : 베이스테이블이 존재하지 않아도 뷰생성가능
  - alias  
        뷰에서 생성할 표현식 이름(테이블의 컬럼이름의미)
        생략하면 서브쿼리의 이름적용
        alias의 갯수는 서브쿼리의 갯수와 동일해야함
  - 서브쿼리 : 뷰에서 표현하는 데이터를 생성하는 select구문
  - 제약조건 
        with check option : 뷰를 통해 접근가능한 데이터에 대해서만 DML작업가능
        with read only : 뷰를 통해 DML작업안됨
        제약조건으로 간주되므로 별도의 이름지정가능


[뷰 - 인라인(inline)개념]  
  : 별칭을 사용하는 서브쿼리 (일반적으로 from절에서 사용)

[뷰 - Top N분석]
  Top N분석 : 조건에 맞는 최상위(최하위) 레코드를 N개 식별해야 하는 경우에 사용
   예) 최상위 소득자3명
         최근 6개월동안 가장 많이 팔린 제품3가지
         실적이 가장 좋은 영업사원 5명

   오라클에서 Top N분석원리
      - 원하는 순서대로 정렬
            - rownum 이라는 가상의컬럼을 이용하여 순서대로 순번부여
            - 부여된 순번을 이용하여 필요한수만큼 식별
                  - rownum값으로 특정행을 선택할수 없음
        (단, Result Set  1st  행(rownum=1)은 선택가능)



# pandas numpy

# 9/28 

random 

---

numpy 데이터의 차원이 확장되거나 차원의 연산이 복잡해질 때 사용한다

![image-20220928144757632](../../images/TIL_day05_220928wen/image-20220928144757632.png)