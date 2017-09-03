# Requirements
```
docker-toolbox https://www.docker.com/products/docker-toolbox
```

# Install development platform 
```
git clone https://github.com/freedomson/playkubo-docker.git
cd playkubo-docker
docker build -f Dockerfile .
docker run -dit -p 8081:8081 --name playkubo #{IMAGE_ID}
docker ps -a
docker attach playkubo
```
