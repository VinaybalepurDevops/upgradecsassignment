FROM maven:3.5.2-jdk-8 as api
RUN mkdir upstac-api-master
COPY ./upstac-api-master /upstac-api-master
WORKDIR /upstac-api-master
RUN mvn clean package install spring-boot:repackage -Pprod
FROM openjdk
WORKDIR /upstac-api-master
COPY --from=api /upstac-api-master/target/upstac-api-0.0.1-SNAPSHOT.jar  /upstac-api-master
EXPOSE 8080
ENTRYPOINT ["java","-jar", "upstac-api-0.0.1-SNAPSHOT.jar"]
