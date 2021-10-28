# docker-todoapp
Sample todo app using docker and Jenkins

## visualize docker in ubuntu
https://www.portainer.io/blog/portainer-your-docker-gui-for-your-ubuntu-linux-desktop
1. sudo docker volume create portainer_data
2. sudo docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-c
