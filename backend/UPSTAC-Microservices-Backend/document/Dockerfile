FROM maven:3.5.2-jdk-8 as build
RUN mkdir upstac-api-document
COPY ./upstac-api-document /upstac-api-document
WORKDIR /upstac-api-document
RUN mvn clean package install spring-boot:repackage -Pprod
FROM openjdk
WORKDIR /upstac-api-document
COPY --from=build /upstac-api-document/target/upstac-api-0.0.1-SNAPSHOT.jar  /upstac-api-document
EXPOSE 8080
ENTRYPOINT ["java","-jar", "upstac-api-0.0.1-SNAPSHOT.jar"]
