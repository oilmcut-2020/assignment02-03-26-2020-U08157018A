# HOW TO INSTALL DOCKER ?

## Manage Docker as non-root user

### To create the docker group and add your user:
1) Create the docker group.
   
        sudo groupadd docker
   
2) Add your user to the docker group.

        sudo usermod -aG docker $USER

3) TYPE :

        newgrp docker
        
4) Verify that you can run docker commands without sudo

        docker run hello-world

# Follow below Steps to install Docker: 

1)Open file install_docker.sh 

**OR**

2) Copy this :
```
#!/bin/bash

sudo apt-get update
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io

sudo docker run hello-world

echo "docker installed !!!"

```
3) Open terminal 
4) Type : 

        nano docker.sh
Please refer below screenshot :             
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d1.png">
</p>

5) Copy the Code from install_docker.sh and paste in  nano docker.sh
Please refer below screenshot :  

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d2.png">
</p>

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d3.png">
</p>

6) Press **Ctrl+S** & **Ctrl+X**
Please refer below screenshot : 
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d4.png">
</p>

7) Type :

        sh docker.sh
Please refer below screenshot : 
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d5.png">
</p>

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d6.png">
</p>

---------------------------------------------------------------------------------------------------------------------------

# HOW TO INSTALL ECLIPSE IN YOUR COMPUTER ?

1) Type :

        echo $DISPLAY
Please refer below screenshot :
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/e1.png">
</p>

2) Type :

        xhost + 
Please refer below screenshot :
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/e2.png">
</p>

3) Type : for eclipse photon version 

        docker run -it -e DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix shivanibaldwa/eclipse:3.0
   
Please refer below screenshot :        

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/e4.png">
</p>

