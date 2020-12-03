# Dockerfile
FROM pinpointdocker/pinpoint-agent:2.1.0 AS base

FROM tomcat:8-jre8-alpine
COPY --from=base /pinpoint-agent /pinpoint-agent
RUN rm -rf /usr/local/tomcat/webapps/*
RUN apk add --no-cache bash curl
EXPOSE 8080
COPY target/*.war /usr/local/tomcat/webapps/ROOT.war
