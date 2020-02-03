https://technology.amis.nl/2018/11/01/running-reactive-spring-boot-on-graalvm-in-docker/

1- cd complete/
2- mvn -Dmaven.compiler.fork=true -Dmaven.compiler.executable="../jdk1.8.0_241/bin/javac" clean package
3- mvn -Dmaven.compiler.fork=true -Dmaven.compiler.executable="../jdk1.8.0_241/bin/javac" dockerfile:build
4- docker run -p 8080:8080 -t springio/gs-reactive-rest-service:latest
