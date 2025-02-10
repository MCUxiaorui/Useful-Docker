# Useful-Docker
## Homeassistant

```
docker pull homeassistant/home-assistant
```
```
sudo docker run -d \
  --name homeassistant \
  -p 8123:8123 \
  homeassistant/home-assistant
```
## Transmission
```
docker run -d \
  --name=transmission \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=America/New_York \
  -p 9091:9091 \
  -p 51413:51413 \
  -p 51413:51413/udp \
  -v ~/docker/transmission/config:/config \
  -v ~/docker/transmission/downloads:/downloads \
  -v ~/docker/transmission/watch:/watch \
  --restart unless-stopped \
  linuxserver/transmission
```
