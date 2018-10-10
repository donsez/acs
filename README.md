# JHipster in Practice (10/10/2018)


@ Home : JHipster installation https://www.jhipster.tech
@ Home : Create a heroku free account https://www.heroku.com/
@ Home : Install cloc https://github.com/AlDanial/cloc

## Generation of blank "monolothic" application (Angular frontend)
* Count the number of lines of code
* Quality of generated code (with SonarQube)
* Run the application : dev onto localhost then deploy prod onto the cloud heroku

## Generating the model of a simple application “myblog”
* Get blog.jh from https://github.com/jhipster/jdl-samples
* Edit JDL with https://start.jhipster.tech/jdl-studio/ (the model can be saved and the application can be generated from the studio if you have a github account.
* Count the number of lines of code (with cloc tool)
* Quality of generated code (with SonarQube tool)
* Run the application : dev onto localhost then deploy prod onto the cloud heroku
* Use the Chrome Devtools for studying the network traffic frontend to backend

## Study of the generated code
* Open the project with your favorite IDE (Eclipse JEE for instance)
* Edit one or two classes
* Count the number of lines of code (with cloc)
* Quality of generated code (with SonarQube)
* Redeploy (localhost then heroku)

## Update JDL
* Add a Comment entity and 2 relationships (with Entry and User)
* Add a Like entity and 2 relationships (with Entry and User)
* Regenerate the application


## Help

### Installation
JavaSE 8, node, npm, yo, yarn
https://www.jhipster.tech/installation/


### Generate the blank application
Term 1
```shell
mkdir myblog
cd myblog
jhipster
./mvn
```

### Generate the entities of myblog
https://www.jhipster.tech/creating-an-entity/

Term 1
```shell
jhipster import-jdl ../acs/myblog.jdl --force
```

### Development
Term 1
```shell
./mvn
```

Term 2
```shell
npm install
yarn start
```

### Production
```shell
./mvnw -Pprod,swagger clean package
./mvnw -Pprod,swagger install -DskipTests
./mvnw spring-boot:run
java -jar target/myblog
```

### Deploy on Heroku
https://www.jhipster.tech/heroku/
