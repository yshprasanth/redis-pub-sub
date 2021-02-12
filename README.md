# Redis Stream Publisher and Consumer App


### Build and Run standalone
1. Install redis from redis.io

    Start redis server:
        ` redis-server `
   
    Start redis-cli and execute below commands:
        ` redis-cli `

    Create a stream using redis command:
        ` XADD purchase-events * dummy-key dummy-value `

    Create a Consumer Group as shown below:
        ` XGROUP CREATE purchase-events purchase-events $ `
   
2. Build using maven command
   
    ` cd redis-pub-sub`
    ` man clean install `
   
3. Launch Producer

    From IDE, start running file RedisStreamProducerApplication 
            OR
    From Command, execute below commands
    ` cd redis-stream-producer `
    ` java -jar target/redis-stream-producer.jar `

4. Launch Consumer

   From IDE, start running file RedisStreamConsumerApplication
   OR
   From Command, execute below commands
   ` cd redis-stream-consumer `
   ` java -jar target/redis-stream-consumer.jar `
   
### Build From Docker

1. Docker Build Consumer

    ` cd redis-stream-consumer `
    ` docker build . `
   
2. Docker Build Producer

   ` cd redis-stream-producer `
   ` docker build . `
   
3. Launch Redis and Redis-Commander

    ` cd redis-pub-sub`
    ` docker-compose up redis redis-commander `

   Access redis-commander from http://localhost:8081
   
   Create a stream using redis command:
    ` XADD purchase-events * dummy-key dummy-value `
   
   Create a Consumer Group as shown below:
    ` XGROUP CREATE purchase-events purchase-events $ `
    
4. Launch Publisher

    ` docker-compose up producer `
   
5. Launch Consumer
   
    ` docker-compose up consumer `