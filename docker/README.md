# Learning Docker

## Commands
To start docker
```
sudo service docker start
```
To download a container/image
```
sudo docker pull <name>
```
To run the container / image
```
sudo docker run -it <name>
```
To pull the images present in the .yml file and build corresponding containers. You should be present in the directory containing the .yml file.
```
sudo docker-compose up -d
```
