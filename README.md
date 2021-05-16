# streaming-etl-pipeline

## Set Up
### Requiments
- Ubuntu 20.04.2.0 LTS
- Java 1.8
- Confluent platform installed
- docker CE
### Config
- change docker-compose KAFKA_ADVERTISED_LISTENERS PLAINTEXT_HOST to your ip 
- guide to set-up postgres, mongo, ksql server and elastic search
(https://docs.ksqldb.io/en/latest/tutorials/etl/#create-the-customers-table-in-postgres)
### How to run
- To start the pipeline run:
``bash
docker-compose up
``
- add more data to mongodb collection "oders" and "shipments" 
- run this to see the loaded shipped_orders joined table already indexed by elastic 
``bash
curl http://localhost:9200/shipped_orders/_search?pretty
``
