

# more info: https://dockerswarm.rocks/traefik/

export EMAIL=andrey.syvrachev@gmail.com
export DOMAIN=registry.yourteams.org
export USERNAME=admin
export PASSWORD=changethis
export HASHED_PASSWORD=$(openssl passwd -apr1 $PASSWORD)


echo $HASHED_PASSWORD

It will look like:
  $apr1$89eqM5Ro$CxaFELthUKV21DpI3UTQO.


Warning!!! For traefik 2.0 -> Yo have to replace each char '$' -> '$$'
