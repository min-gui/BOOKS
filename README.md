# sql-tuning

## 업무에 바로 쓰는 SQL 튜닝

<img width="200" alt="image" src="https://contents.kyobobook.co.kr/sih/fit-in/458x0/pdt/9791162244500.jpg">

## 정리
## 목차

* [1. MySQL과 MariaDB개요](#1-MySQL과 MariaDB개요)
  * [구조적 차이](#구조적-차이)
---
## 1. MySQL과 MariaDB개요


버전 찾기
```sql
SHOW VARIABLES LIKE 'version%';
SELECT @@version;
```


### 구조적 차이
- Oracle
  - 통합된 스토리지 하나를 공유.
  - 사용자가 어느 DB 서버에 접속 하여 작업 하더라도 같은 결과 출력, 동일한 구문 CRUD
  를 처리할 수 있다.
- MySQL
  - 물리적인 DB 서버 마다 독립적으로 스토리지를 할당.
  - 마스터 - 슬레이브 (주-종 구조) 가 대부분. 마스터는 쓰기/읽기 가능, 슬레이브는 읽기만 
  가능. 여러대 DB 서버에 접속해서 CRUD를 실행하더라도 처리되지 않을 수 있다.
  - 상대적인 낮은 메모리 사용.
  - 중첩 루프 조인 알고리즘만으로 풀림.

  
  *_쿼리 오프로딩_  
  트랜잭션 쓰기(UPDATE, INSERT, DELETE) ,읽기(SELECT) 분리하여 처리량 증가 기법






