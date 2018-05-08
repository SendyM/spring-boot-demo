FROM frolvlad/alpine-oraclejdk8
VOLUME /tmp
MAINTAINER lovelysendy <daijkl@qq.com>

RUN apt-get update; \
    apt-get -y upgrade

RUN apt-get -y install g++ cmake git subversion

RUN mkdir /home/git; \
    cd /home/git; \
    sudo git clone https://github.com/SendyM/spring-boot-demo.git -b master; \
    cd spring-boot-demo; \
    mvn clean;\
    mvn package

ADD spring-boot-demo-1.0.1.jar app.jar

RUN sh -c 'touch /app.jar'
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]