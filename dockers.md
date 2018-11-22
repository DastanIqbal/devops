### Install docker
#### https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
#apt-cache policy docker-ce
sudo apt-get install -y docker-ce
#sudo systemctl status docker //check docker status
sudo usermod -aG docker ${USER}
su - ${USER}
#id -nG //list user group
sudo usermod -aG docker <username>
```

### Search images
```
docker search <image_name>
```

### Pull images 
```
docker pull <image_name>
```

### Run contianer
```
docker run -it alpine //foreground and interactive

docker run -d -p 81:80 -v $PWD/src:/var/www --name="container_name" image_name //background
```

### Open bash in running container
```
docker exec -it <container id> /bin/bash
```

### List running containers
```
docker ps -l
```

### Save docker progress
```
docker commit containerId alpine-nginx
```

### List Images
```
docker images
```

### Share code or directory between host & directory
```
docker run -v ~/<path>/src:/www -p 81:80 -it alpine-nginx
```

### Remove Docker Images
```
docker rmi <imageId>
```
### Create Tag
```
docker tag bb38976d03cf hubusername/imagename:tagname
```

### Push docker to hub
```
docker push hubusername/imagename
```

### Save Locally
```
docker save imagename > imagename.tar
```

### Load local image
```
docker load --input imagename.tar
```

### Error: requested access to the resource is denied
```
docker tag bb38976d03cf hubusername/imagename:tagname
```

```
docker push hubusername/imagename
```

