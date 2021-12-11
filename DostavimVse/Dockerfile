FROM openjdk:8
WORKDIR /DostavimVse
COPY . .
RUN apt-get update 
RUN apt-get install dos2unix
RUN dos2unix mvnw
RUN ./mvnw -Pinit-base -DskipTests clean package
CMD java -jar ./target/dostavimvse-0.0.1-SNAPSHOT.jar 
CMD ./mvnw -Pweb-app -DskipTests clean package 
CMD java -jar ./target/dostavimvse-0.0.1-SNAPSHOT.jar --server.port=8080

