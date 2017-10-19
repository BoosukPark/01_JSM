# 01_JSM
Docker compose
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

# update repository url 
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

# Package update
sudo apt-get update

# install docker
sudo apt-get install docker-ce

# Docker version check
sudo docker info
