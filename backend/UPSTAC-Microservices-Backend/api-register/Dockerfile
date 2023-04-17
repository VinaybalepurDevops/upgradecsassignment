FROM maven:3.5.2-jdk-8 as api
RUN mkdir upstac-api-register
COPY ./upstac-api-register /upstac-api-register
WORKDIR /upstac-api-register
RUN mvn clean package install spring-boot:repackage -Pprod
FROM openjdk
WORKDIR /upstac-api-register
COPY --from=api /upstac-api-register/target/upstac-api-0.0.1-SNAPSHOT.jar  /upstac-api-register
EXPOSE 8080
ENTRYPOINT ["java","-jar", "upstac-api-0.0.1-SNAPSHOT.jar"]
