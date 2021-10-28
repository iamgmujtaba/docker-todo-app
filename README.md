# docker-todoapp
Sample todo app using docker and Jenkins on Ubuntu

## docker installation
https://docs.docker.com/engine/install/ubuntu/

## visualize docker in ubuntu
https://www.portainer.io/blog/portainer-your-docker-gui-for-your-ubuntu-linux-desktop
```shell
sudo docker volume create portainer_data
sudo docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-c
```shell

You can now open your prefered browser, in my case its Firefox, and connect to 
http://localhost:9000


## To run todo-app on docker
```shell
sudo docker build -t todo-app .
sudo docker run -dp 3000:3000 todo-app
```shell

## Jenkins Installation

```shell
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins

sudo systemctl daemon-reload
sudo systemctl start jenkins
sudo systemctl status jenkins

sudo ufw allow 8080
sudo ufw status
```shell




