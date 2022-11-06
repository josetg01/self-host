# Installation

```
git clone https://github.com/atareao/self-hosted.git
cd self-hosted/yacht
mv sample.env .env
sed -i "s/yacht.tuservidor.es/el_fqdn_que_quieras/g" .env
mkdir yacht
```

A la hora de levantar el servicio dependerá del proxy inverso que hayas seleccionado. Si has elegido Caddy, simplemente,

```
docker-compose -f docker-compose.yml -f docker-compose.caddy.yml up -d
docker-compose logs -f
```

Las credenciales por defecto son,

```
usuario: admin@yacht.local
password: pass
```
