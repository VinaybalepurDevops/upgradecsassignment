# upgradassignment
# Upgrad labs application

An application to register for medical lab activites

## Getting started

Download [Docker Desktop](https://www.docker.com/products/docker-desktop) for Mac or Windows. [Docker Compose](https://docs.docker.com/compose) will be automatically installed. On Linux, make sure you have the latest version of [Compose](https://docs.docker.com/compose/install/).

Once these are installed follow the steps
```
 * Create docker images for backend, frontend and mysql database
 * Tag and Push the images to AWS ECR
 * Use these images in the ECS applation
 ```
 Use the following environment variables in the ECS containers
 ```
    Mysql
    database_name  -> upgradpg
    database_password -> upgradpg
    database_username -> upgradpg
    MYSQL_ROOT_PASSWORD	 -> root
    Open port 3306

    Document service
    MYSQL_HOST	-> private ip of the mysql service
    Open port -> 8082

    Master service
    MYSQL_HOST	-> private ip of the mysql service
    Open port -> 8080

    Register service
    MYSQL_HOST	-> private ip of the mysql service
    Open port -> 8090
``` 
