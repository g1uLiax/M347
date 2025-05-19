# A.)

<img width="832" alt="image" src="https://github.com/user-attachments/assets/61372d10-300e-4a18-a2aa-f8f6aa6d3368" /><br>

<img width="937" alt="image" src="https://github.com/user-attachments/assets/26107287-8c43-4f4f-9c1c-ac57a85296c6" /><br>
<img width="836" alt="image" src="https://github.com/user-attachments/assets/52c2e37a-e5b8-4247-8412-0a971814d8de" /><br>


`docker build -t g1uliax/m347:kn02a -f Dockerfile .` <br>
`docker run -d --name kn02a -p 80:80 g1uliax/m347:kn02a` <br>
`docker push g1uliax/m347:kn02a` <br>

```Dockerfile
FROM nginx    
# use the latest nginx image
WORKDIR /usr/share/nginx/html/
# set the working directory
COPY helloworld.html .
# copy things from the static html directory
EXPOSE 	80	  
# expose the port 80

```

# B.)
## Database
<img width="610" alt="image" src="https://github.com/user-attachments/assets/f5e104ba-7c98-4b73-87d7-c29137a672ba" /><br>

`docker build -t g1uliax/m347:kn02b-db -f Dockerfile-db .` <br>
`docker run -d --name kn02-db -p 3306:3306 g1uliax/m347:kn02b-db` <br>

```Dockerfile
FROM mariadb

ENV MARIADB_ROOT_PASSWORD=1234
ENV MARIADB_DATABASE=m346db
ENV MARIADB_USER=admin
ENV MARIADB_PASSWORD=1234

EXPOSE 3306
```

## Webserver
