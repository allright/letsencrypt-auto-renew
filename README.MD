

1. copy docker-compose.yaml to your server
2. ssh to your server, and setup environment variables:

```
export EMAIL=email@gmail.com
export DOMAIN=registry.yourdomain.org
export USERNAME=admin
export PASSWORD=changethis
export HASHED_PASSWORD=$(openssl passwd -apr1 $PASSWORD)
```

```
echo $HASHED_PASSWORD
```
It will look like:
```
$apr1$89eqM5Ro$CxaFELthUKV21DpI3UTQO.
```

#Warning!!! For traefik 2.0
You have to replace each char '$' -> '$$'
example:
```
$apr1$89eqM5Ro$CxaFELthUKV21DpI3UTQO.
```
will be changed to:
```
$$apr1$$89eqM5Ro$$CxaFELthUKV21DpI3UTQO.
```
3. install docker
```
apt install docker.io
```
4. switch to docker swarm mode
```
docker swarm init
```
5. deploy
```
docker stack deploy -c ./docker-compose.yaml reg
```



more info: https://dockerswarm.rocks/traefik/
