# emart-app

Launch a EC2 instance 
Ubuntu OS
Put the above script in advance option 


#!/bin/bash

### Install docker on Ubuntu
sudo apt-get update
   sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release -y
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
   echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

### Install docker-compose
   sudo apt-get update
   sudo apt-get install docker-ce docker-ce-cli containerd.io -y
   sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
   sudo chmod +x /usr/local/bin/docker-compose

### Add ubuntu user into docker group
    sudo usermod -a -G docker ubuntu





then login in to the EC2 instance 
ssh -i Downloads/dockerkey.pem unbuntu@ipadress
id
We just need to fetch the source code and use

the Docker Compose file to build and on our container.

So we'll say git clone, get the URL.

You should have the repository clone here.
git clone  URL

Cd emartapp

docker--compose build
Docker images
docker-compose up 
docker-compose up -d
docker-compose down
