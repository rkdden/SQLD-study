# SQL 기본
## SQL 문장 종류
* 데이터 조작어(DML): SELECT, INSERT, UPDATE, DELETE
* 데이터 정의어(DDL): CREATE, ALTER, DROP, RENAME
* 데이터 제어어(DCL): GRANT, REVOKE
* 트랜잭션 제어어(TCL): COMMIT, ROLLBACK

## 단일행 NULL 관련 함수 종류
* NVL(표현식1, 표현식2) / ISNULL(표현식1, 표현식2) : 표현식1의 결괏값이 NULL이면 표현식2의 값을 출력한다.
* NULLIF(표현식1, 표현식2): 표현식1이 표현식2와 같으면 NULL을, 같지 않으면 표현식1을 리턴한다.
* COALESCE(표현식1, 표현식2, ...): 임의의 개수 표현식에서 NULL이 아닌 최초의 표현식을 나타낸다. 모든 표현식이 NULL이라면 NULL을 리턴한다.

## 정렬
* ASC: 오름차순
* DESC: 내림차순

## 집계 함수의 종류
* COUNT(*): NULL을 포함한 행의 수를 출력
* COUNT(표현식): 표현식의 값이 NULL 값인 것을 제외한 행의 수를 출력
* SUM(): 표현식의 NULL 값을 제외한 합계를 출력
* AVG(): 표현식의 NULL 값을 제외한 평균을 출력
* MAX(): 표현식의 최댓값 출력
* MIN(): 표현식의 최솟값 출력
* STDDEV(): 표준편차 출력
* VARIAN(): 분산 출력

## 단일행 문자형 함수의 종류
* LOWER(문자열): 문자열의 알파벳 문자를 소문자로 바꾸어준다.
* UPPER(문자열): 문자열의 알파벳 문자를 대문자로 바꾸어 준다.
* ASCII(문자): 문자나 숫자를 ASCII 코드 번호로 바꾸어 준다.
* CHR/CHAR(ASCII번호): ASCII 코드 번호를 문자나 숫자로 바꾸어 준다.
* CONCAT(문자열1, 문자열2): Oracle, MySQL에서 유효한 함수이며 문자열1과 문자열2를 연결한다. 합성연산자 '| |'(Oracle)이나 '+'(SQL Server)와 동일하다.
* SUBSTR/SUBSTRING (문자열, m[, n ]): 문자열 중 m위치에서 n개의 문자 길이에 해당하는 문자를 돌려준다. n이 생략되면 마지막 문자까지이다.
* LENGTH/LEN(문자열): 문자열의 개수를 숫자값으로 돌려준다.
* LTRIM(문자열[, 지정문자]): 문자열의 첫 문자부터 확인해서 지정 문자가 나타나면 해당 문자를 제거한다. (지정문자가 생략되면 공백 값이 디폴트) SQLServer에서는 LTRIM 함수에 지정문자를 사용할 수 없다. 즉, 공백만 제거할 수 있다.
* RTRIM(문자열[, 지정문자]): 문자열의 마지막 문자부터 확인해서 지정 문자가 나타나면 해당 문자를 제거한다. (지정문자가 생략되면 공백 값이 디폴트) SQLServer에서는 RTRIM 함수에 지정문자를 사용할 수 없다. 즉, 공백만 제거할 수 있다.
* TRIM([leading|trailing|both]지정문자 FROM 문자열): 문자열에서 머리말, 꼬리말, 또는 양쪽에 있는 지정 문자를 제거한다. (leading|trailing|both가 생략되면 both가 디폴트) SQL Server에서는 TRIM 함수에 지정문자를 사용할 수 없다. 즉, 공백만 제거할 수 있다.
