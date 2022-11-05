```yaml
---
version: "2.1"
services:
  homeassistant:
      image: ghcr.io/home-assistant/home-assistant:stable 
      container_name: homeassistant
      environment:
        - PUID=1000
        - PGID=1000
        - TZ=TZ=Africa/Johannesburg
      volumes:
        - /root/homeassistant:/config
      networks:
        - host
      restart: unless-stopped
```
