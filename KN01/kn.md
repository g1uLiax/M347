# A.)
`wsl --status # Sie erhalten dann Auskunft über die aktuelle Version von WSL`<br>
`wsl --update # Aktualisieren Sie ihre WSL-Installation`<br>

`docker run -d -p 80:80 docker/getting-started` <br>  
<img width="923" alt="image" src="https://github.com/user-attachments/assets/7aa8fefa-88f7-4482-a4ea-37a929d2e964" /><br>

# B.)
`docker --version`<br>
`docker search ubuntu`, `docker search ubuntu/nginx`<br>

`-d` stands for detach, this means that when we run the container it will do it in the background and we wont have an open terminal that we need to keep open for the container to run.<br>
`-p` stands for port, with this parameter we can determine which ports the container uses. (outside:inside)<br>

`docker pull nginx`<br>
`docker create --name nginx -p 8081:80 nginx`<br>
`docker start nginx`<br>

<img width="1127" alt="image" src="https://github.com/user-attachments/assets/92dbd4f6-f5b4-4039-9cee-f25169915eae" /><br>

`docker run -d ubuntu` pulls the image from the repository and creates a container. The container couldnt be started since we didnt specify a port. Without the missing parameters the container runs detached.<br>
`docker run -it ubuntu` starts the container and you enter the its command line, when exiting you also stop the container. It stands for interactive terminal. <br>

<img width="1127" alt="image" src="https://github.com/user-attachments/assets/3423ae39-2181-4238-ad1e-c19c23aed187" /><br>
`docker ps`<br>
`docker stop nginx` <br>

`docker rm -f $(docker ps -aq)` remove all containers, -f for force stop<br>
<img width="984" alt="image" src="https://github.com/user-attachments/assets/07064f48-1715-46b1-95fc-1346b66171e0" /><br>
`docker rm name`<br>

<img width="655" alt="image" src="https://github.com/user-attachments/assets/35087573-c42b-48d4-901e-7574c6ea9668" /><br>
`docker images`<br>
`docker rmi nginx`<br>

# C.)
<img width="914" alt="image" src="https://github.com/user-attachments/assets/488abcaa-8014-4ffe-af65-29324d0684e5" />

# D.)
tag and push a dockerimage to a repository. <br>
`docker tag nginx:latest g1uliax/m347:nginx` nginx images is now named g1uliax/m347 with the tag nginx  <br>
`docker push g1uliax/m347:nginx` push the image with the tag nginx to the repository <br>

<img width="912" alt="image" src="https://github.com/user-attachments/assets/f2d2c774-9acb-424a-8d4e-c99abceeb435" /><br>







