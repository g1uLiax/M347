## KN04

Builds, (re)creates, starts, and attaches the services to a container<br>
<img width="522" alt="image" src="https://github.com/user-attachments/assets/9342ff17-02c5-4e17-b9db-f995ceacfb22" /><br>

Parses the docker-compose.yml file<br>
- Reads all service, network, volume, and build configurations.<br>


Build the Dockerfile if needed, pull the image if needed, create a network, create the container and then start it. connect the containers to the defined networks.<br>
docker build <br>
docker pull<br>
docker network create<br>
docker create<br>
docker start<br>
docker network connect<br>

