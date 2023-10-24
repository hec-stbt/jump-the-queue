# Creates backend image
# ....................................
# First stage: build the Java application
FROM maven:3.6.3-openjdk-11-slim AS build
WORKDIR /backend
COPY jtqj .
RUN mvn clean install
RUN mvn package

# Second stage: copy the built app from the first stage
FROM openjdk:11-slim
WORKDIR /backend
COPY --from=build /backend/server/target/jtqj-server-bootified.war .
EXPOSE 80
CMD ["java", "-jar", "jtqj-server-bootified.war"]