# 방송국 DB 설계
SBS 방송국 프로그램 정보를 데이터베이스로 직접 본다면?

<br />

## 프로젝트 개요
- 방송국 내 드라마, 예능 프로그램 정보와 프로그램에 참여한 연예인, 제작진 정보를 쉽게 찾아볼 수 있는 데이터베이스 제작
- ERD를 설계하고 DB를 구현하여, 직접 제작한 쿼리로 다양한 결과를 출력
- 직접 ERD를 설계하고 DB를 구현함으로써 무결성, 유연성, 확장성을 고려한 효율적인 데이터베이스를 제작
- 직접 쿼리를 제작함으로써 데이터베이스를 다양한 방법으로 출력하고 활용

## 도구
Oracle DB, Toad Data Modeler

## 기간
2023.05.12 - 2023.06.12

## ERD
KOR.ver
![ERD](https://github.com/na-kyoung/DB_SBS/assets/137421820/4d565dfd-94c0-4456-a834-c3f7cd6dee9e)

ENG.ver
![ERD_eng](https://github.com/na-kyoung/DB_SBS/assets/137421820/e328f159-215d-4c2f-998d-721f65ae5ce3)

## 테이블 소개
- Drama : 드라마 프로그램 정보 (드라마이름, 방영연도, 방영시간, 회차)
- Drama_genre : 드라마 장르
- Viewer_ratings : 시청률 (최고 시청률, 최저 시청률)
- Entertainment : 예능 프로그램 정보 (예능이름, 방영시작연도, 방영종료연도, 방영시간)
- AudienceRating : 시청 등급
- broadcastDay : 방영 요일
- ProductionCrew : 제작진 정보 (직원이름, 업무, 연봉)
- Production : 제작진 참여 정보 (직무)
- Department : 제작진 부서 정보 (부서명)
- Celebrity : 연예인 정보 (연예인이름, 생년월일, 성별, 개런티, 데뷔연도, 키)
- Appear : 연예인 출연 정보 (역할)
- Agency : 연예인 소속사 정보 (소속사명)

## 쿼리 제작 결과
>본인이 제작한 쿼리만 작성하였습니다.

1. 1970년도 이전에 데뷔한 연예인의 이름, 나이, 데뷔연도, 소속사를 출력하시오. (단, 나이는 생년월일로 계산해야 함.)

   <img width="755" alt="1_1970전데뷔" src="https://github.com/na-kyoung/DB_SBS/assets/137421820/577318c3-673f-4893-8a68-df680c27ef38">

2. 감독 주동민이 연출한 드라마명, 장르, 최고 시청률을 출력하시오.

   <img width="497" alt="2_감독주동민" src="https://github.com/na-kyoung/DB_SBS/assets/137421820/55c2007e-a454-4957-a432-c71fe15fcf58">

3. 2017년도에 방영한 예능의 이름, 연출에 참여한 스태프 이름과 직업을 출력하시오. (단, 스태프ID로 직업을 PD/작가로 구분해야 함.)

   <img width="496" alt="3_2017방영예능" src="https://github.com/na-kyoung/DB_SBS/assets/137421820/a47b49b3-8708-49de-87b8-410b56168485">

4. 작가 김은숙이 집필한 드라마 중 최고 시청률이 20이상인 드라마명, 출연 배우, 배우의 페이를 출력하시오. (단, 페이=회차별 개런티*드라마 회차로 구해야 함.)

   <img width="509" alt="4_작가김은숙" src="https://github.com/na-kyoung/DB_SBS/assets/137421820/d4e34007-e0df-423f-b640-7680eeae3683">

5. BH엔터테인먼트 소속인 여배우의 이름, 출연 드라마명, 최고 시청률, 최저 시청률을 출력하시오.

   <img width="623" alt="5_BH엔터" src="https://github.com/na-kyoung/DB_SBS/assets/137421820/97c59b8a-1389-4fd7-b36b-40f7e1f60682">
