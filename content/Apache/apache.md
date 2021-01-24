# APACHE

[![HOME](../../img/button_home.png)](https://github.com/mmmarceleza/My-Learning-Tracker#marcelos-learning-tracker) &nbsp; &nbsp; [![MY ARTICLES](../../img/button_article.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/my-articles.md#my-articles) &nbsp; &nbsp; [![PORTFOLIO](../../img/button_portfolio.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/portfolio.md#portfolio) &nbsp; &nbsp; [![LEARNING LOG](../../img/button_log.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/learning-log.md#learning-log)

***

## Completed Courses:

|   | Courses | Certificate |
|:---:|:---:|:---:|
| ![Apache](../../img/apache_logo.png) | [Apache Web Server: Administration](https://www.linkedin.com/learning/apache-web-server-administration) | [Certificate](https://www.linkedin.com/in/marcelomarquesmelo/) |

## Introduction

Apache is one of the most famous web server available and widely used on the web. It is free, open source, one of the oldest and most reliable web server. It is also robust and has many integrations with other popular softwares.

## Install Apache on Ubuntu

First, update your repository:
```bash
$ sudo apt update
```
Then, install apache package:
```bash
$ sudo apt install apache2
```
If you have a Firewall, adjust it to allow outside access to the default web ports.

## Managing the Service

After the installation on Ubuntu, Apache starts automatically. Check if the Apache service is running in `systemd` with the following command:
```bash
$ sudo systemctl status apache2
```
Check the defaults ports with `nestat` command:
```bash
$ netstat -tupan | grep -i apache
```

## Apache configuration file

- Fedora and CentOS: `/etc/httpd/conf/httpd.conf`
- Debian and Ubuntu: `/etc/apache2/apache2.conf`

## Useful commands

- Command to verify the status of the server:
```bash
$ apachectl -t
```


## References

- https://youtu.be/rCr3-YlL5S8?t=574
- https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-18-04

