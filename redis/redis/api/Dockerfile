FROM eclipse-temurin:21.0.1_12-jre-alpine

COPY api-*.jar /opt/api.jar

USER root

EXPOSE 8080

RUN mkdir -p /logs

CMD ["java", "-jar", "/opt/api.jar"]

# HEALTHCHECK --interval=60s --timeout=3s CMD curl --silent --fail --request GET http://localhost:8080/actuator/health | grep '"status":"UP"' || exit 1
