# List of Commands Applied per Avtivity

## IT 311 Laboratory Activity on September 24, 2025
- sudo groupadd **Groupiee**
- cat /etc/group
- sudo usermod -aG **Groupiee** **christinejoyagkis**
- sudo usermod -g **Groupiee** **christinejoyagkis**
- grep **Groupiee** /etc/group
- sudo useradd **ECBacay**
- sudo passwd **ECBacay**
- sudo useradd **FValencia**
- sudo passwd **FValencia**
- cat /etc/group
- sudo usermod -aG **Groupiee** **ECBacay**
- sudo usermod -g **Groupiee** **ECBacay**
- sudo usermod -aG **Groupiee** **FValencia**
- sudo usermod -g **Groupiee** **FValencia**
- cat /etc/group
- grep **Groupiee** /etc/group

## IT 311 Laboratory Activity on September 25, 2025

Docker Ubuntu Environment
- docker pull ubuntu
- docker run -it ubuntu
- apt update
- apt install -y sudo
- apt install -y passwd

Linux Commands
- sudo useradd -m **student1**
- sudo passwd **student1**
- sudo groupadd **group1**
- sudo usermod -aG **group1** **student1**
- grep **group1** /etc/group
- grep **student1** /etc/passwd

## IT 311 Laboratory Activity on October 08, 2025
- mkdir **Testing**
- cd **Testing**
- sudo useradd **Admin1**
- sudo passwd **Admin1**
- sudo useradd **Staff1**
- sudo passwd **Staff1**
- sudo useradd **Staff2**
- sudo passwd **Staff2**
- sudo useradd **Staff3**
- sudo passwd **Staff3**
- sudo usermod -aG sudo **Admin1**
- getent passwd **Admin1 Staff1 Staff2 Staff3**
- groups **Admin1**
- mkdir -p **Backup**
- cd **Backup**
- cd ..
- sudo chown -R Admin1:Admin1 **Backup**
- sudo chmod -R 770 **Backup**
- su **Admin1**
- whoami
- df -h 
- df -h > **Backup/disk_usage.txt** 
- free -m  
- free -m > **Backup/memory_usage.txt**
- top
- q
- top -n 1 > **Backup/top_processess.txt**
- ps aux
- ps aux > **Backup/ps_aux.txt** 
- ls **Backup**
- sudo apt update | tee **Backup/update_log.txt**

## IT 311 Laboratory Activity on October 23, 2025
- uptime
- ps aux
- df -h
- free -h
- sudo apt install htop
- htop
- q
- tail -n 20 /var/log/syslog

## IT 311 Laboratory Activity on October 29, 2025
- docker pull ubuntu
- docker run -dit --name **node1** ubuntu bash
- docker run -dit --name **node2** ubuntu bash
- docker exec **node1** apt update -y
- docker exec **node1** apt install iputils-ping -y
- docker exec **node2** apt update -y
- docker exec **node2** apt install iputils-ping -y
- docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' **node1**
- docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' **node2**

## IT 311 Laboratory Activity on November 5, 2025
- docker pull ubuntu
- docker run -dit --name **node1** ubuntu bash
- docker run -dit --name **node2** ubuntu bash
- docker exec **node1** apt update -y && docker exec **node1** apt install iputils-ping -y
- docker exec **node2** apt update -y && docker exec **node2** apt install iputils-ping -y
- docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' **node1**
- docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' **node2**
- docker exec **node1** ping **172.17.0.3**
- Ctrl + C
- docker network create **peer_net**
- docker network ls
- docker run -dit --network **peer_net** --name **peer1** ubuntu bash
- docker run -dit --network **peer_net** --name **peer2** ubuntu bash
- docker exec **peer1** apt update -y && docker exec **peer1** apt install iputils-ping -y
- docker exec **peer2** apt update -y && docker exec **peer2** apt install iputils-ping -y
- docker exec **peer1** ping **peer2**
- Ctrl + C
- docker network ls
- docker network inspect **peer_net**
