# SQL (Structured Query Language)

SQL은 주로 관계형 데이터베이스 에서 사용하는 언어로 데이터베이스에 쿼리를 보내 원하는 데이터를 가져올수 있다.

# 데이터베이스 명령어

끝에 ; 필수
* 데이터베이스 생성

        create database 데이터베이스 이름;

* 데이터베이스 조회 

        show databases;

* 데이터베이스 선택 

        use 데이터베이스 이름;

* 테이블 생성 (데이터베이스를 선택 한 후에 실행해야한다)

        CREATE TABLE user (
        id int PRIMARY KEY AUTO_INCREMENT,
        name varchar(255),
        email varchar(255)
        );

    user라는 테이블을 생성하고 필드는 id, name, email이다. 필드 다음으로 필드 타입을 설정해준다.

* 특정 테이블 정보조회

        describe 테이블 이름;


# SQL명령어

* select(특성 조회)

        select 특성(e.g. id);

* from(어느 테이블에서 가져올지 명시)

        select id from user // user테이블에서 id칼럼을 조회

* where(조회할 값을 필터링 해줌)

        select id from user where age < 40 // age가 40보다 적은 id를 조회

* order by(특정 값을 정렬해서 출력)

        select * from user order by age // user 테이블의 모든 정보를 age 기준으로 오름차순 정렬

        select * from user order by age desc // 내림차순으로 정렬

* limit(조회할 정보의 수 제한)

        select * from user limit 10 // user 테이블에서 모든 정보를 10개만 조회
