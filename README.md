# apache-hadoop

Finding the top 5 airlines with the greatest average DEPARTURE_DELAY using Apache Hadoop MapReduce with MrJob python package.

## Requirements

* [Docker 24+](https://www.docker.com/get-started)

## Bootstraping your environment
* Download datasets from [Kaggle](https://www.kaggle.com/datasets/usdot/flight-delays?select=flights.csv) and put them to "apache-hadoop/dataset/" folder

```sh
$ docker-compose up -d
# wait while environment initialization is complete
$ ./run.sh
# will install all necessary packages and move dataset to hdfs
$ docker exec -t apache-hadoop-namenode-1 chmod u+x /my_volume/main.py 
```
## Run
```
docker exec -t apache-hadoop-namenode-1 python3 /my_volume/main.py -r hadoop hdfs:///flights.csv
```

