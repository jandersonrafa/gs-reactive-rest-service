https://technology.amis.nl/2018/11/01/running-reactive-spring-boot-on-graalvm-in-docker/

1º cd complete/
mvn -Dmaven.compiler.fork=true -Dmaven.compiler.executable="../jdk1.8.0_241/bin/javac" clean package
mvn -Dmaven.compiler.fork=true -Dmaven.compiler.executable="../jdk1.8.0_241/bin/javac" dockerfile:build
docker run -p 8080:8080 -t springio/gs-reactive-rest-service:latest
