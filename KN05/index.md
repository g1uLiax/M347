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
