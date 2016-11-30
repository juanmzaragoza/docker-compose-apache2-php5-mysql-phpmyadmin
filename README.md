# Docker-compose: Apache2 + PHP5 + MySQL

This docker compose runs an apache server with php5 and mysql with an admin with phpmyadmin

## Overview

When starting to develop a PHP project, we need to build a web server with php installed, configure its virtualhost, install a database, configure it and so on. 
Having docker-compose and this basic structure, we can up any project in an extremely fast time.

## Getting Started

In the root's project run

```
docker-compose up --build
```

### Prerequisites

We need install the nexts dependencies:

* [Docker Engine](https://docs.docker.com/engine/installation/) - The docker itself
* [Docker Compose](https://docs.docker.com/compose/install/) - For defining and running multi-container Docker applications

### Distribution of directories

The following directory structure fully describes the project
```
.
+-- docker-compose.yml
+-- docker
|   +-- mysql
|   +-- sites-enabled
|   	+-- vhost.conf
|   +-- Dockerfile
+-- public_html
```

Inside docker/mysql will be stored the bases created by our project. Then DON'T DELETE IT.
Inside docker/sites-enabled is the configuration of the server where we will install our project.
Inside public_html is all our php project.

### Adaptation to the project

To adapt it to your project, you must copy the content into the public_html folder.

Then, you can modify the docker-compose to map different ports, assign different ip, bind different folders, etc..

## Authors

* **Juan Manuel Zaragoza** - *Initial work* - [juanmzaragoza](https://github.com/juanmzaragoza)
