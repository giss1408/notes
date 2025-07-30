# Toutes mes notes [md doc](https://www.markdownguide.org/cheat-sheet/) and [md doc2](https://www.markdownguide.org/basic-syntax/)

## Docker

### Setup  docker for Ubuntu
	- sudo apt-get install apt-transport-https ca-certificates
	- curl gnupg-agent software-properties-common

	- curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

	- sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

	- sudo apt-get update
	- sudo apt-get install docker-ce docker-ce-cli containerd.io

	- sudo systemctl enable docker && systemctl start docker

	- sudo groupadd docker
	- sudo usermod -aG docker $USER

### List all images
    - docer ps -a
    - docker ps -f
    - docker rm
    - docker images -f
    - docker rmi
    - docker volume ls
    - docker volume rm
    - docker system prune

### Docker at Dormakaba
    - Connect to image repo: 
        docker login artifactory.dormakaba.net
    - Get image from repo: 
        docker pull artifactory.dormakaba.net/pd-emea-cr-core-docker-local/dev-images/beme/clip-master-sdk:latest
    -   Run docker to compile sdk:  
        docker run -it --rm -v /home/dev/Development/sdk_17_11/porthos-devicesdk:/home/dev/devicesdk artifactory.dormakaba.net/pd-emea-cr-core-docker-local/dev-images/beme/clip-master-sdk:latest

---
## Ubuntu not reachable from local network
	- disable firewall: sudo ufw disable

---
## Github and git
### Github authentication
    - git-credential-manager login github

### Github commit
	- git add README.md
	- git commit -m "first commit"
	- git branch -M main
	- git remote add origin https://github.com/giss1408/notes.git
	- git push -u origin main

### Some cmds
    - git log --graph --decorate
    - git grep -w "search" "search_dir"

---
## Flutter development
	- flutter doctor
	- flutter pub get : install dependencies
	- fluutter upgrade : upgrade dart SDK version

	- flutter run
	- flutter pub cache clean

---
## Nodejs development
* sudo npm install to install dependencies inside project

---
## Old project bonnivoire run inside docker with old npm and nodejs versions todo

---
## heroku
* no email and passwd, use API key

--
## Free images for commercial use
    * https://www.shutterstock.com/
### AI Tool opensource
    - PremierPro = Openshot
    - ChatGpt4 = Copilot
    - Midjourney = Leonardo
    - Jasper = writesonic
    - Captions AI = veed.io
    - Synthesia = Simplified //
    - Photoshop = Photopea // photo editing
    - ElevenLabs = Lovo AI // Voice

---    
## Name of Symboles
	- ~: TILDE
	- -: HYPHEN / dash

---
## Python stuffs
    - Create virtual env: python -m venv /path/to/new/virtual/environment
    - Activate source env/bin/activate

---
## <span style="color:red;">Projet</span>
	- creating a client code generation tool for a Flutter app 

## Java
	- sudo ln -sfn /usr/local/opt/openjdk/bin/java /Library/Java/JavaVirtualMachines/openjdk24.jdk
	- java -version

### Compile
	- Compile the program: javac HelloWorld.java
	- Run the program: java HelloWorld

### locate java
	- To find the Java bin path, use the command readlink -f $(which java)



## Some helpful commands
    # kill unresponsive ssh session: ENTER + ~ .
### Store date time 
    - hwclock -uw /dev/rtc0

    - strace -e ioctl /opt/dormakaba/xxxx

    - sscanf("%[^.].%[^.].%[^=]%s",var)

### Certificate info
    - openssl x509 -text -noout -in ~/Downloads/Porthos\ Root\ CA\ 1.crt 

### Verify cert again root
    - openssl verify -verbose -show_chain -crl_check_all -CAfile NonProdCAVert.pem AliceCert.pem
