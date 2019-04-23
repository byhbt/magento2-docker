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

Then download source code magento from https://github.com/tomasinchoo/m2-sample.docker/tree/master
put to the **html** directory

Rename the **.env.example** to **.env**, review the config in **.env** and change if you need. 

### Step 2: Up the environment

```
docker-compose up
```

Run sample magento command from  host

```
docker-compose exec apache-php php bin/magento setup:upgrade
```

## Contributing

Free to make pull request. 

## Links

* [Bug Tracker & QA](https://github.com/byhbt/magento2-docker/issues)
