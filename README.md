Simple docker compose file built as an exercise and also in order to be able to follow [Complete SQL Mastery](https://codewithmosh.com/p/complete-sql-mastery) available at [codewithmosh.com](https://codewithmosh.com). First three hours of the course are available on Youtube as [MySQL Tutorial for Beginners](https://youtu.be/7S_tz1z_5bA).
Tested with docker version 24.0.2 and docker compose 2.18.1.

## Template

Sets up a mysql container and a php-admin container in a new docker network. First time template is run, persistent volumes for both container will be created.  Mysql container may take a bit longer to become available the first time. __This is a very simple template lacking any security or scalability__.

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

![Antares connection set up](https://github.com/javierjsa/mysql-compose/blob/main/antares_login.png?raw=true)
     
 Access mysql container:
 
    docker exec -ti mysql /bin/bash
    
 If you ever want to start from scratch, delete mysql volume:
 
    docker volume rm mysql-volume
    
## Credits

- [Connect to mysql running in docker container from a local machine](https://towardsdatascience.com/connect-to-mysql-running-in-docker-container-from-a-local-machine-6d996c574e55)
- [How to install docker compose on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-20-04)
- [Docker compose file reference v3](https://docs.docker.com/compose/compose-file/compose-file-v3/)


