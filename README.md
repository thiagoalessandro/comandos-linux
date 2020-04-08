# Comandos linux

## Leitura de arquivo via http
```
curl -H "Authorization: Basic dC5hbGVzc2FuZHJvOlRoaWFnMEAwNzAzMT=" https://${host}
watch -n 5 "wget --user ${user} --password ${password} -qO-  https://${host} | grep INFO | tail" 
```
## Permissão Postgres
```sql
create user app with password 'app@070335';
GRANT ALL PRIVILEGES on SCHEMA public to app;
```
## S3

Sincroniza
```
aws s3 sync s3://.../logs/kubernetes/pp-tcb/citiconnector . --exclude "*"  --include "*2020-04-08*"
```
Visualizar
```
zcat * | sed -r 's/([0-9]+-[0-9]+-[0-9]+[A-Z][0-9]+:[0-9]+:[0-9]+[A-Z])\t.*\t\{/{"time":"\1",/g' | jq -r '[.time,.log] | "\(.[0]) \(.[1])"' | grep -v ^$ | grep 2876012495859541796

```
