# Envoy TCP over HTTP tunneling
used for spiking envoy TCP tunnel over HTTP

### Topology
This using 4 service
- echo-redis, an HTTP server that connect to Envoy TCP
- envoy-client, accept TCP, and tunneling this via HTTP
- envoy-server, accept HTTP, and forward to redis as TCP
- redis, awesome redis

### Usage
- start all services
```
make up
```

- try to curl echo-redis
```
curl 172.19.0.2/redis/{key}
```
