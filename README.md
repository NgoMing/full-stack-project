# Full-stack Project

## Description
* Implement full stack web step by step
* Basic components:
  - Front-end: programming language and its libraries + frameworks
  - Server: Nginx ( or Apache)
  - Back-end: programming language and its framework
  - Database: Realational or Non-relational database and appropriate language and data management

## Environment
### Configure shared folder between Window and Docker environment
* Guide link: https://stackoverflow.com/questions/30040708/how-to-mount-local-volumes-in-docker-machine
* Commands
```
cd mnt/sda1/var/lib/boot2docker
sudo vi bootlocal.sh

sudo mkdir -p /home/minhnln/vboxshare
sudo mount -t vboxsf -o defaults,uid=`id -u docker`,gid=`id -g docker` CloudAssignment /home/minhnln/vboxshare
```

### System requirements
* Window OS
* Docker Toolbox: https://docs.docker.com/toolbox/toolbox_install_windows/
* Docker version: 18.03
* Docker-machine version 0.14.0
* Docker-compose version 1.20.1

### Implementation
#### Nginx
* Reference [nginx serve static file](https://github.com/arunkumars08/docker-static-files-serve)
* Using docker compose + dockerfile
  - nginx-dockerfile: declare dependencies, and ports
  - docker-compose.yml: create container, link ports, volumes and command
* Goals: 
  - move changealbe part to docker-compose => more flexible
  - create volume for html folder which is content of the page
  - create volume for config folder which is for configuration of nginx server