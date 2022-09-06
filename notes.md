# Toutes mes notes

## Docker

### Setup Ubuntu
sudo apt-get install apt-transport-https ca-certificates
curl gnupg-agent software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

sudo systemctl enable docker && systemctl start docker

sudo groupadd docker
sudo usermod -aG docker $USER


### Github
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/giss1408/notes.git
git push -u origin main


