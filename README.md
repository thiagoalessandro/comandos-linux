# Comandos linux

## Leitura de arquivo via http

curl -H "Authorization: Basic dC5hbGVzc2FuZHJvOlRoaWFnMEAwNzAzMT=" https://${host}

watch -n 5 "wget --user ${user} --password ${password} -qO-  https://${host} | grep INFO | tail" 

## Permissão Postgres

create user app with password 'app@070335';

GRANT ALL PRIVILEGES on SCHEMA public to app;
