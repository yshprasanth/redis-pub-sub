# Use JRE11 slim
FROM openjdk:14.0-jre-slim

# Add the app jar
ADD target/redis-stream-consumer-0.0.1-SNAPSHOT.jar redis-stream-consumer.jar

ENTRYPOINT java -jar redis-stream-consumer.jar