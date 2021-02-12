# Use JRE11 slim
FROM openjdk:11.0.5-jre-slim

# Add the app jar
ADD target/redis-stream-producer-0.0.1-SNAPSHOT.jar redis-stream-producer.jar

ENTRYPOINT java -jar redis-stream-producer.jar