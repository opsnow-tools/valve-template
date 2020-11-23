# Dockerfile
FROM pinpointdocker/pinpoint-agent:2.1.0 AS base

FROM openjdk:8-jre-alpine
ENV JAVA_OPTS="-XX:+UnlockExperimentalVMOptions -XX:+UseCGroupMemoryLimitForHeap"
COPY --from=base /pinpoint-agent /pinpoint-agent
RUN apk add --no-cache bash curl
EXPOSE 8080
WORKDIR /data
ENTRYPOINT exec java $JAVA_OPTS -jar ROOT.jar
COPY ./target/*.jar /data/ROOT.jar
