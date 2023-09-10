# Toutes mes notes

## Docker

### Setup  docker for Ubuntu
sudo apt-get install apt-transport-https ca-certificates
curl gnupg-agent software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

sudo systemctl enable docker && systemctl start docker

sudo groupadd docker
sudo usermod -aG docker $USER

### Ubuntu not reachable from local network
* disable firewall: sudo ufw disable

### Github
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/giss1408/notes.git
git push -u origin main

### Flutter
* flutter doctor
* flutter pub get : install dependencies
* fluutter upgrade : upgrade dart SDK version

### Nodejs
* sudo npm install to install dependencies inside project


### Old prject bonnivoire run inside docker with old npm and nodejs versions todo

### heroku
* no email and passwd, use API key


