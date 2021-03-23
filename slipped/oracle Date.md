# SQL 사용 시 DATE 관련 이것저것

#### TO_DATE & TO_CHAR
- CHAR -> DATE
```
TO_DATE('{CHAR}', '{FORMAT}')
```
- DATE -> CHAR
```
TO_CHAR({DATE},'{FORMAT}')
```
  
- FORMAT 예시  
  - 24시간 YYYYMMDDHH24MISS  
  - 12시간 YYYYMMDDHH12MISS

#### SQL DEVELOPER 시간 출력 수정
환경설정 -> 데이터베이스 -> NLS -> 날짜형식에 FORMAT 입력
