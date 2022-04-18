## installation
Добавить алиас в профиль\
alias sail='[ -f sail ] && bash sail || bash vendor/bin/sail'
```sh
mkdir Development
cd Development
curl -s "https://laravel.build/example-app?with=mysql,redis&devcontainer" | bash
sudo systemctl stop mariadb.service nginx.service php-fpm7.service
```
<br>

## sail start/stop
```sh
cd example-app
sail up -d
sail stop
```
http://localhost/
<br><br>


## sail simple command
```sh
sail php --version
sail node --version
sail yarn
```
<br>

## xdebug
<p>
.env <br>
SAIL_XDEBUG_MODE=develop,debug
</p>

```sh
docker ps --format 'table {{.Names}}\t{{.Ports}}'
docker inspect -f {{range.NetworkSettings.Networks}}{{.Gateway}}{{end}} <container-name>
```
