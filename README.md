# Some Spark Standalone Clusters through Docker examples

Reviewed few docker compose files which creates a spark standalone cluster with for development in pyspark. Some pointers about them are listed below.


## Prerequisites:
1. Docker 
2. Docker-compose

## Installation
1. https://docs.docker.com/engine/install/
2. If Docker Desktop is donloaded then docker-compose is installed by default.
3. If Docker is installed in a linux system, install docker-compose separately.

## Examples 
### 1. bitnami-docker-spark

- Pyspark works right out of the box
- Completely customizable 
- No sudo access for the master node
- Documentation: [docs](bitnami-docker-spark/README.md)


### 2. docker-spark-cluster

- Pyspark does not work right out of the box
- Some windows encoding problems encountered with \r in start-spark.sh
- Does not use HDFS
- Documentation: [docs](docker-spark-cluster/README.md)


### 3. docker-spark-standalone

- Not Direct command (No docker compose) each worker has to be started individually
- Pyspark works right out of the box
- Mounts directory 
- Does not use HDFS
- Documentation: [docs](docker-spark-standalone/README.md)


### 4. spark-standalone-cluster-on-docker

- Pyspark works right out of the box
- Mounts directory 
- Uses JupyterLab (if required)
- Uses HDFS
- Documentation: [docs](spark-standalone-cluster-on-docker/README.md)