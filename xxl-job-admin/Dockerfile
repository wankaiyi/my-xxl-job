FROM openjdk:8-jdk-slim
MAINTAINER wankaiyi

COPY --from=hengyunabc/arthas:latest /opt/arthas /opt/arthas

ENV PARAMS=""

ENV TZ=PRC
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ADD target/xxl-job-admin-2.5.0-SNAPSHOT.jar /app.jar

ENTRYPOINT ["sh","-c","java -jar $JAVA_OPTS /app.jar $PARAMS"]