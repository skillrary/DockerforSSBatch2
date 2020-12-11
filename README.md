# DockerforSSBatch2



sudo su -

yum update

sudo yum install -y yum-utils device-mapper-persistent-data lvm2

yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

yum install docker-ce docker-ce-cli containerd.io



docker version

systemctl start docker




## Create Dockerfile. (Dockerfile name should be Dockerfile under a folder. 
##Create a directory and create a file with following contents)

```text
FROM ubuntu
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get -y install apache2
ADD . /var/www/html
ENTRYPOINT apachectl -D FOREGROUND
ENV name DEVOPS SKILLRARY
```

## Create a html file by name a.html

```html
<p>Welcome to&nbsp;<strong>Skill</strong>Rary</p>
<p>I love <strong>Skill</strong><span style="color: #00ff00;">Rary</span></p>
<p><span style="color: #00ff00;"><img src="https://www.skillrary.com/uploads/images/fav-sr-64x64-logo.png" alt="" width="64" height="64" /></span></p>
```

##Execute the command below.
```dockerfile
docker build -t skillrary_dockerfile .
```
##here skillrary_dockerfile will be the image name when its gets created. Once this is done one has to start the container on a port to access tomcat. 


