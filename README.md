# docker-sensu
Docker and Sensu (big friends)

# pablolibo@gmail.com

# Docker-compose example:

## client

```json
client
  image: pablolibo/sensu-docker:1.0.0-1
  environment:
    CLIENT_NAME: "${HOSTNAME}"
    CLIENT_SUBSCRIPTIONS: all
    CLIENT_ADDRESS: "${HOSTNAME}"
    REDIS_HOST: 10.0.0.6
    REDIS_PORT: 6379
    REDIS_PASSWORD: ""
    REDIS_DB: 0
    REDIS_AUTO_RECONNECT: "true"
    REDIS_RECONNECT_ON_ERROR: "false"
  volumes:
    - /:/mnt/disk:ro
  ports:
    - '3030:3030'
  command: client
```
