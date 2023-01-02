# Some Spark Standalone Clusters through Docker examples

Reviewed few docker compose files which creates a spark standalone cluster with for development in pyspark. Some pointers about them are listed below.

## Prerequisites:
1. Docker 
2. Docker-compose

## Installation
1. https://docs.docker.com/engine/install/
2. If Docker Desktop is donloaded then docker-compose is installed by default.
3. If Docker is installed in a linux system, install docker-compose separately.


## Use

1. Clone the Repo
	```
	git clone https://github.com/cluster-apps-on-docker/spark-standalone-cluster-on-docker
	```

2. Move into the directory. 
	```
	$ cd spark-standalone-cluster-on-docker
	```

### spark-standalone-cluster-on-docker

Few features which make this dockerfile useful.
- Pyspark works right out of the box
- Mounts directory 
- Uses JupyterLab (if required)
- Uses HDFS

To start with default configuration: 
```
docker-compose up -d
```

After this the cluster can be maanged by using the Docker Desktop GUI. We can use it to Start, Stop, Delete cluster or open the jupyterlab in browser (which is available at [localhost:8888](http://localhost:8888))

To create More number of workers, copy paste the worker part of code in docker-compose.yml and change the importatn features like tag, name and ports.

## Build Docker-Compose
To change the build configuration, a Unix based system or WSL is required to run [build.sh](spark-standalone-cluster-on-docker/build/build.sh).

```
cd build
vim build.yml
```

Edit YMl file with required configuration. Then run the build.sh file to get docker compose file.

```
chmod +x build.sh
./build.sh
```




Futher Documentation: [docs](spark-standalone-cluster-on-docker/README.md)