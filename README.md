# Jenkins repo

## Docker commands

```
docker network create jenkins

docker build -t myjenkins:1.1 .

docker run --name jenkins --rm --detach
  --network jenkins --env DOCKER_HOST=tcp://docker:2376
  --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1
  --volume jenkins-data:/var/jenkins_home
  --volume jenkins-docker-certs:/certs/client:ro
  --publish 8080:8080 --publish 50000:50000 myjenkins:1.1
  
docker logs jenkins
```