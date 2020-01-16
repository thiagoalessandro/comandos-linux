# Comandos linux

## Leitura de arquivo via http

curl -H "Authorization: Basic dC5hbGVzc2FuZHJvOlRoaWFnMEAwNzAzMTY=" https://${host}

watch -n 5 "wget --user ${user} --password ${password} -qO-  https://uat-tcb.tfs.totvs.com/tcbseguranca-log/log/catalina.out | grep INFO | tail" 
