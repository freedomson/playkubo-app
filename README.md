# Install development platform 
```
git clone https://github.com/freedomson/playkubo-docker.git
cd playkubo-docker
docker build -f Dockerfile .
docker run -dit -p 8081:8081 #{IMAGE_ID}
docker ps -a
docker attach #{CONTAINER_ID}
```
