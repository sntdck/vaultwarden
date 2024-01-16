# vaultwarden
Configuration vaultwarden
first we need to configurate docker-compose.yml and custom nginx configuration file custom.conf
1. docker file create in home/containers/docker-compose.yaml
2. custom nginx file create by path /etc/nginx/conf.d/custom.conf
when you make any changes, don't forget to reload the files 
second it is create ssl certificate if you didn`t have that you need follow some steps 
1. sudo openssl req -x509 -nodes -days 365 -newkey rsa:4096 -keyout /etc/ssl/private/vaultwarden.key -out /etc/ssl/certs/vaultwarden.crt  # if you need you can change the name of file to another
2. sudo openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048
