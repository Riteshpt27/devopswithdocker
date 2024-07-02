FROM amazoncorretto:8-alpine3.16

EXPOSE 8080

WORKDIR /usr/src/app

RUN apk add --no-cache dos2unix

COPY . .

RUN dos2unix mvnw 

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]