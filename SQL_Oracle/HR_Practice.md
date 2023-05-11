1. 직책(Job Title)이 Sales Manager인 사원들의 입사년도와 입사년도(hire_date)별 평균 급여를 출력하시오. 출력 시 년도를 기준으로 오름차순 정렬하시오. 

```sql
SELECT TO_CHAR(e.HIRE_DATE,'YYYY'), AVG(e.SALARY)
FROM JOBS j, EMPLOYEES e 
WHERE j.JOB_ID = e.JOB_ID AND j.JOB_TITLE = 'Sales Manager'
GROUP BY TO_CHAR(e.HIRE_DATE,'YYYY') 
ORDER BY TO_CHAR(e.HIRE_DATE,'YYYY') ASC;
```

