# Requirements
```
docker-toolbox https://www.docker.com/products/docker-toolbox
android-studio
androidSDK
```

# Install development platform 
```
git clone https://github.com/freedomson/playkubo-docker.git
cd playkubo-docker
# TODO: Push a proper docker image to dockerhub.com
docker build -f Dockerfile .
docker run -dit -v #{HOST_FOLDER}:/host-map-folder -p 8081:8081 --name playkubo #{IMAGE_ID}
```
# Run react-native packager
```
docker attach playkubo
cd playkubo-app
react-native start
# Get your docker-machine ip
docker-machine ip
# Check your react-native packager from host machine
http://#{DOCKER_MACHINE_IP}:8081
```
# Set up device
```
# Connect your device to host via usb and activate wifi
adb tcpip 5555
# Disconnect usb and connect via Wifi from host
adb connect #{DEVICE_IP}:5555
# Set up VM
Open Oracle VM VirtualBox Manager
Select the VM used by Docker
Click Settings -> Network
Adapter 1 should (default?) be "Attached to: NAT"
Click Advanced -> Port Forwarding
Add rule: Protocol TCP, Host Port 8080, Guest Port 8080 (leave Host IP and Guest IP empty)
You should now be able to browse to your container via localhost:8080 and your-internal-ip:8080.
```
