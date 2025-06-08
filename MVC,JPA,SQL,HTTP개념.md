## MVC(Model-View-Controller)
- 서버 역할을 분담해 처리하는 기법

## JPA(Java Persistence API)
- 서버와 DB 간 소통에 관여하는 기술

## SQL(Structured Query Language)
- DB 데이터를 관리하는 언어

## HTTP(HyperText Transfer Protocol)
- 데이터를 주고받기 위한 통신 규약
- 대표 메서드(POST,GET,PATCH(or PUT) : 데이터 수정 요청,DELETE)

## CRUD를 위한 SQL문과 HTTP 메서드
| 작업 (기능)    | SQL 문         | HTTP 메서드        | 설명                                          |
| ---------- | ------------- | --------------- | ------------------------------------------- |
| 생성(Create) | `INSERT INTO` | `POST`          | 새로운 데이터 생성                                  |
| 읽기(Read)   | `SELECT`      | `GET`           | 데이터 조회                                      |
| 수정(Update) | `UPDATE`      | `PUT` / `PATCH` | 기존 데이터 수정<br>`PUT`: 전체 수정<br>`PATCH`: 일부 수정 |
| 삭제(Delete) | `DELETE FROM` | `DELETE`        | 데이터 삭제                                      |
