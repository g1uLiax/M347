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

