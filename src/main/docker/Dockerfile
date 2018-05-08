FROM frolvlad/alpine-oraclejdk8
VOLUME /tmp
MAINTAINER lovelysendy <daijkl@qq.com>

ADD spring-boot-demo-1.0.1.jar app.jar

RUN sh -c 'touch /app.jar'
#RUN sh -c "./configure"
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]