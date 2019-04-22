# Magento 2 Docker

This code from the tutorial https://inchoo.net/magento-2/development-environment-magento-2-using-docker/


### How to use

```
git clone git@github.com:byhbt/magento2-docker.git
```

Then download source code magento from https://github.com/tomasinchoo/m2-sample.docker/tree/master
put to the **html** directory

Rename the **.env.example** to **.env**, review the config in **.env** and change if you need. 


```
docker-compose up
```

Run sample magento command:

```
docker-compose exec apache-php php bin/magento setup:upgrade
```
