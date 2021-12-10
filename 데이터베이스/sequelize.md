# sequelize 

sequelize 는 ORM(Object-Relational-Mapping)을 도와주는 모듈로 관계형 데이터베이스에 있는 entities나 record에 접근할때 객체나 class처럼 다룰수 있게 도와준다.

* sequelize 다운로드

        npm install --save sequelize

* sequelize cli 다운로드

        npm install --save-dev sequelize-cli

* bootstraping(프로젝트 초기단계 자동 설정)

        npx sequelize-cli init

    bootstraping을 하면 
    
    config/config.js

    models/index.js

    migration

    seeders

    파일, 폴더들이 생성된다. 

* 모델 생성

        npx sequelize-cli model:generate --name User --attributes firstName:string,lastName:string,email:string

    name은 모델의 이름, attributes는 생성할 필드를 써주면 된다. 

    위처럼 작성하면 models 폴더에 User파일이 생기는데 그 안에 attributes의 내용이 객체로 들어간다. 

    필드들의 데이터타입은 string으로 지정되어있는데 다른 데이터 타입을 넣고싶다면 (https://sequelize.org/master/manual/model-basics.html#data-types)참조

* migration

    지금까지 모델을 만들었다면 이제 migration을 해서 데이터베이스에 이 데이터들을 테이블로 넣어줘야 한다. 

    데이터베이스는 따로 생성해야 하고 만들어야 할 데이터베이스는 config.js 참고.

        npx sequelize-cli db:migrate

