Simple docker compose file built as an exercise and also in order to be able to follow 'Complete SQL Mastery' available at codewithmosh.com. 
Tested with docker version 24.0.2 and docker compose 2.18.1.

## Template

Sets up a mysql container and a php-admin container in a new docker network. First time template is run, persistent volumes for both container will be created.  Mysql container mat take a bit longer to become available the first time. This is a very simple template lacking any security or scalability.

## Usage

Deploy:

    docker compose up

Tear down:

    docker compose down
    
Default user and password:

    user: root
    password: 123
        
Connect to php-admin using a browser:

    http://0.0.0.0:82
    
Alternatively, a db client such as Antares may be used:

![alt text](https://github.com/javierjsa/mysql-compose/blob/main/antares_login.png?raw=true)
    
 
 Access mysql container:
 
    docker exec -ti mysql /bin/bash
    
