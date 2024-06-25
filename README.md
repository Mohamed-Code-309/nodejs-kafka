# nodejs-kafka
Create a basic Node.js project that produce and consume messages with **Kafka**.


### App Summary:

1. Files
   -  **`producer.js`** : responsible for produce random messages to Kafka Cluster.
   - **`consumer.js`** : responsible for reading messages from Kafka Cluster.
   - **`docker-compose.yml`** : start up Kafka cluster with 3 brokers.

2. Packages 
   - In this app we used two different **NPM** packages: 
     - **`kafkajs`**: API for communication between NodeJS and the Kafka cluster.
     - **`chance`**: to generate random animal names and produce them as values in different messages.


### How to run: 
1. make sure to install nodejs on your machine https://nodejs.org/en/
2. open the app in **VS Code** and run in terminal : ```npm install``` to install dependancies
3. starting up Kafka cluster with 3 brokers using the `docker-compose.yml` file by running in terminal : `docker-compose up -d`
   - make sure docker is installed as well: https://www.docker.com/products/docker-desktop/
4. to start produce some messages run: `node produce.js`
   - If you see here error in the console that tells me that there is no leader for this topic and we were not able to produce message this one because topic was just created and there was no leader elected yet, just retry to execute the command again `node produce.js`
5. to start consume the produced messages  run: `node consumer.js`
