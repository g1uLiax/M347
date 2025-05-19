# A.)

<img width="832" alt="image" src="https://github.com/user-attachments/assets/61372d10-300e-4a18-a2aa-f8f6aa6d3368" />

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
