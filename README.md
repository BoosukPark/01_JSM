# Docker 
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

# update repository url 
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

# Package update
sudo apt-get update

# install docker
sudo apt-get install docker-ce

# Docker version check
sudo docker info


# docker compose

version: '3.0'
services:
  web:
    image: alicek106/composetest:web
    ports:
      - "80:80"
    links:
      - mysql:db
    command: apachectl -DFOREGROUND
  mysql:
    image: alicek106/composetest:mysql
    command: mysqld
