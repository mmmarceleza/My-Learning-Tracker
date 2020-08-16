# DOCKER

[![HOME](../../img/button_home.png)](https://github.com/mmmarceleza/My-Learning-Tracker#marcelos-learning-tracker) &nbsp; &nbsp; [![MY ARTICLES](../../img/button_article.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/my-articles.md#my-articles) &nbsp; &nbsp; [![PORTFOLIO](../../img/button_portfolio.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/portfolio.md#portfolio) &nbsp; &nbsp; [![LEARNING LOG](../../img/button_log.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/learning-log.md#learning-log)

***

## Completed Courses:

|   | Courses | Certificate |
|:---:|:---:|:---:|
| ![Docker](../../img/docker-alura.png) | [Docker: Criando containers sem dor de cabeça](https://cursos.alura.com.br/course/docker-e-docker-compose) | [Certificate](https://cursos.alura.com.br/certificate/2b0189ad-54fa-4016-b05d-a0e2bad1464c) |

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
Create a new container:
```bash
docker run name_of_the_container
```
Check all created containers 
```bash
docker ps -a
```

