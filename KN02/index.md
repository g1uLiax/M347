# A.)

<img width="832" alt="image" src="https://github.com/user-attachments/assets/61372d10-300e-4a18-a2aa-f8f6aa6d3368" /><br>

<img width="937" alt="image" src="https://github.com/user-attachments/assets/26107287-8c43-4f4f-9c1c-ac57a85296c6" /><br>

`docker build -t g1uliax/m347:kn02a -f Dockerfile .` <br>
`docker run -d --name kn02a -p 80:80 g1uliax/m347:kn02a` <br>
`docker push g1uliax/m347:kn02a` <br>

```
FROM nginx    
# use the latest nginx image
WORKDIR /usr/share/nginx/html/
# set the working directory
COPY helloworld.html .
# copy things from the static html directory
EXPOSE 	80	  
# expose the port 80

```
