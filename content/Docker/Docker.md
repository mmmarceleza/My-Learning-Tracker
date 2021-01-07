# DOCKER

[![HOME](../../img/button_home.png)](https://github.com/mmmarceleza/My-Learning-Tracker#marcelos-learning-tracker) &nbsp; &nbsp; [![MY ARTICLES](../../img/button_article.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/my-articles.md#my-articles) &nbsp; &nbsp; [![PORTFOLIO](../../img/button_portfolio.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/portfolio.md#portfolio) &nbsp; &nbsp; [![LEARNING LOG](../../img/button_log.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/learning-log.md#learning-log)

***

## Completed Courses:

|   | Courses | Certificate |
|:---:|:---:|:---:|
| ![Docker](../../img/docker-alura.png) | [Docker: Criando containers sem dor de cabeça](https://cursos.alura.com.br/course/docker-e-docker-compose) | [Certificate](https://cursos.alura.com.br/certificate/2b0189ad-54fa-4016-b05d-a0e2bad1464c) |
| ![Docker](../../img/linuxacademy.png) | [Docker Quick Start](https://acloudguru.com/course/docker-quick-start) | [Certificate](https://linuxacademy.com/profile/u/cert/id/407900) |

## Install Docker on Manjaro
First step, update the system:
```bash
$ sudo pacman -Syu
```
Next, install Docker using the following command:
```bash
$ sudo pacman -S docker
```
After installation, start the service and enable it to run whenever the system is rebooted:
```bash
$ sudo systemctl start docker.service
$ sudo systemctl enable docker.service
```
To verify if everything is correct, check the version of Docker
```bash
$ sudo docker version
```
To see more information about your Docker installation, there's a simple way:
```bash
$ sudo docker info
```
By default , Docker needs root's privileges to run. To change this behavior, add your user to Docker's group:
```bash
$ sudo usermod -aG docker $USER
```
Reboot your system for those changes to take effect.
## Basic Commands
Create a container (without starting it):
```bash
docker create [IMAGE]
```
Rename an existing container:
```bash
docker rename [CONTAINER_NAME] [NEW_CONTAINER_NAME]
```
Run a command in a new container:
```bash
docker run [IMAGE] [COMMAND]
```
 - `docker run --rm [IMAGE]` - removes a container after it exits.
 - `docker run -td [IMAGE]`-  starts a container and keeps it running.
 - `docker run -it [IMAGE]`- starts a container, allocates a pseudo-TTY connected to the container’s stdin, and creates an interactive bash shell in the container.
 - `docker run -it-rm [IMAGE]`- creates, starts, and runs a command inside the container. Once it executes the command, the container is removed.
Delete a container (if it is not running):
```bash
docker rm [CONTAINER]
```
Update the configuration of one or more containers:
```bash
docker update [CONTAINER]
```
## Starting and Stopping Containers
Start a container:
```bash
docker start [CONTAINER]
```
Stop a running container:
```bash
docker stop [CONTAINER]
```
Stop a running container and start it up again:
```bash
docker restart [CONTAINER]
```
Pause processes in a running container:
```bash
docker pause [CONTAINER]
```
Unpause processes in a running container:
```bash
docker unpause [CONTAINER]
```
Block a container until others stop (after which it prints their exit codes):
```bash
docker wait [CONTAINER]
```
Kill a container by sending a SIGKILL to a running container:
```bash
docker kill [CONTAINER]
```

https://phoenixnap.com/kb/list-of-docker-commands-cheat-sheet

https://www.docker.com/sites/default/files/d8/2019-09/docker-cheat-sheet.pdf


Create a new container:
```bash
docker run name_of_the_container
```
Check all created containers 
```bash
docker ps -a
```

