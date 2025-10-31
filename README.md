# MailHog docker-compose env 

This is how to install Mailhog on linux server

## Prerequisites
- Docker should be instaled
- Docker service should start when server start

## Ports
- web ui on port 8025 with login and password that we have set 
- smtp on port 2025 with login="" and password=""

## Change login and password

 `printf "login:" > mailhog.auth`
 
 `printf "$(sudo docker exec  mailhog /bin/sh -c "MailHog bcrypt password")" >> mailhog.auth`
  - mailhog - name of docker container mailhog

 `cat mailhog.auth`

To create container
 `docker-compose up -d`

