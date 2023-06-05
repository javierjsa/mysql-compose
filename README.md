Simple docker compose file built as an exercise and also in order to be able to follow 'Complete SQL Mastery' available at codewithmosh.com. 
Tested with docker version 24.0.2 and docker compose 2.18.1.

## Template

Sets up a mysql container and a php-admin container. First time template is run, persistent volumes for both container will be created. Mysql container mat take a bit longer to become available the first time.

Deploy:

docker compose up

Tear down:

dokcer compose down