FROM gradle:jdk17-alpine
WORKDIR /api-gateway

COPY ../src /api-gateway/src/
COPY ../build.gradle .

RUN gradle clean build -x test

ENTRYPOINT ["java","-jar","./build/libs/api-gateway-1.0.0.jar"]