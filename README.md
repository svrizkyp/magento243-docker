
# Project Title

Docker image that contains multiple services for Magento 2.4.3

# Services
- PHP 7.4
- Nginx
- Mysql 8

# Additional Services
- Elasticsearch 7.17.18

# How To Run
- Run "docker pull docker.elastic.co/elasticsearch/elasticsearch:7.17.18" to download elasticsearch image
- Run "docker run -p 127.0.0.1:9200:9200 -p 127.0.0.1:9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.17.18" to start elasticsearch
- Run "docker network create -d bridge svr-network" to create custom network
- Clone the repository
- Run "docker-compose build" to build the image
- Run "docker-compose up -d" to start the image
- Run "docker-compose down" to stop the image
- Run "docker-compose exec image-name bash" to enter image bash

# MySQL Default Credential
- Username : root
- Password : example

# MySQL Native Password Auth
- Run "ALTER USER 'youruser'@'%' IDENTIFIED WITH mysql_native_password BY 'yourpassword';"

# Docker network
- Create your custom network by running "docker network create -d bridge yournetworkname"
- Change network_mode value in docker-compose.yml with you custom network name


