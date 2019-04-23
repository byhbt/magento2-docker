# Magento 2 Docker

This code from the tutorial https://inchoo.net/magento-2/development-environment-magento-2-using-docker/

Then made some improvements:
- Increase PHP Memory.
- Update docs for new developer easy to use. 

## How to use

```
git clone git@github.com:byhbt/magento2-docker.git
```
### Step 1:

Then download source code Magento from https://github.com/tomasinchoo/m2-sample.docker/tree/master
put to the directory which just cloned above. 

Rename the **.env.example** to **.env**, review the config in **.env** and change if you need. 

Then update hosts file in **/etc/hosts**

```
127.0.0.1       m2.docker www.m2.docker
```

### Step 2: Up the environment

```
docker-compose up
```

Install composer depdendencies inside the docker container apache-php

```
docker-compose exec apache-php composer install
```

### Step 3: Web setup

Then go to the web browser to start the normal installation proceess via website http://m2.docker

## Common issues

### Conflict with existing port on host pc

```
ERROR: for phpmyadmin  Cannot start service phpmyadmin: driver failed programming external connectivity on endpoint magento2docker_phpmyadmin_1 (767fe572a4e2b34e2de5182e821a6d60f6ec76a9c33e04ebafae8b2433dbfc39): Bind for 0.0.0.0:8081 failed: port is already allocated
ERROR: Encountered errors while bringing up the project.
```
Please update the port in **docker-compose.yml**

### Authentication for Magento repositories

```
 - Installing magento/composer (1.2.0): Downloading (100%)         
 - Installing magento/module-catalog-sample-data (100.2.0): Downloading (connec                           
    Authentication required (repo.magento.com):
      Username: 
```

Login to the Magento.com then get the Public key and Secret key on **Marketplace > Access Keys**, then paste 
Public key ~ username
Private key ~ password

### Run sample magento command from host

```
docker-compose exec apache-php php bin/magento setup:upgrade
```

## Contributing

Free to make pull request. 

## Links

* [Bug Tracker & QA](https://github.com/byhbt/magento2-docker/issues)
