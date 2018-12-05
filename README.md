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
* Window Os
* Docker Toolbox: https://docs.docker.com/toolbox/toolbox_install_windows/
* Docker version: 18.03
* Docker-machine version 0.14.0
* Docker-compose version 1.20.1
