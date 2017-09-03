# Requirements
```
docker-toolbox https://www.docker.com/products/docker-toolbox
```

# Install development platform 
```
git clone https://github.com/freedomson/playkubo-docker.git
cd playkubo-docker
# TODO: Push a proper docker image to dockerhub.com
docker build -f Dockerfile .
docker run -dit -p 8081:8081 --name playkubo #{IMAGE_ID}
```
# Run react-native packager
```
docker attach playkubo
cd playkubo-app
react-native start
# Get your docker-machine ip
docker-machine ip
# Check your
http://#{DOCKER_MACHINE_IP}:8081
```
