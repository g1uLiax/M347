## KN04

Builds, (re)creates, starts, and attaches the services to a container
<img width="522" alt="image" src="https://github.com/user-attachments/assets/9342ff17-02c5-4e17-b9db-f995ceacfb22" />

Parses the docker-compose.yml file
- Reads all service, network, volume, and build configurations.


Build the Dockerfile if needed, pull the image if needed, create a network, create the container and then start it. connect the containers to the defined networks.
docker build 
docker pull
docker network create
docker create
docker start
docker network connect

