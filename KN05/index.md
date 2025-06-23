# A.)

<img width="865" alt="image" src="https://github.com/user-attachments/assets/9f5af958-13d7-4ee5-b38b-1e4e74b1a656" /><br>

```
docker run --name nginx-bindtest -it --rm -v C:\VSC\school\m347\docker-mount:/mnt nginx /bin/bash

Im Container:
cd /mnt
chmod +x test.sh
./test.sh
```
# B.)

<img width="688" alt="image" src="https://github.com/user-attachments/assets/5aa492dc-e8ec-4ebe-a66b-6b4fdc80ff96" />


```
docker volume create shared-data

docker run --name container1 -it -v shared-data:/data nginx /bin/bash
docker run --name container2 -it -v shared-data:/data nginx /bin/bash

Container 1:
echo "Hallo von Container 1 – $(date)" >> /data/log.txt
cat /data/log.txt

Container 2:
echo "Grüsse von Container 2 – $(date)" >> /data/log.txt
cat /data/log.txt
```
# C.)
```
version: '3.9'
services:
  nginx1:
    image: nginx
    volumes:
      - type: volume
        source: shared-volume
        target: /shared
      - type: bind
        source: ./bindvol
        target: /usr/share/nginx/html
      - type: tmpfs
        target: /tmpfs
  
  nginx2: 
    image: nginx
    volumes:
      - shared-volume:/shared

volumes:
  shared-volume:
```

## Start
<img width="887" alt="image" src="https://github.com/user-attachments/assets/60c584b4-d32f-4f94-a3ee-386df114642c" />

## Mount nginx1

<img width="892" alt="image" src="https://github.com/user-attachments/assets/06c62a4d-05cf-4aca-9241-1b8904d4c753" />

## Mount nginx2

<img width="894" alt="image" src="https://github.com/user-attachments/assets/fc549e78-6b68-42b9-a912-2b6d458ef86e" />
